### **System Engineering Context & Hardware Specification**

* **OS:** CachyOS (Arch-based) / Ubuntu 25.10 (Transitioning)
* **Kernel:** `linux-cachyos` / 6.17+ generic
* **Desktop/Display:** GNOME 49.0 on Wayland
* **CPU:** AMD Ryzen 5 7535HS (6-core, 12-thread, Zen 3+, with AVX2 support)
* **GPU:** NVIDIA GeForce RTX 2050 Mobile (4 GB VRAM, Turing architecture, Driver 580+)
* **iGPU:** AMD Radeon 680M / 660M (RDNA-2)
* **System RAM:** 16 GB DDR5 (14.33 GiB available)
* **Storage:** 512 GB Micron NVMe SSD (~140 GiB unallocated space for local models)
* **Primary Interaction Method:** 100% Hands-Free Voice and Screen Capture. No manual texting or switching.

---

### **Core Constraints & Strategy**

* **The VRAM Bottleneck:** With only 4 GB of VRAM, dynamic hot-swapping or running separate task-specific models (e.g., switching between a coder model and a math model) causes massive latency spikes (5–10 seconds per swap).
* **The Hybrid Solution:** Run a single Multimodal Vision-Language Model (VLM) pinned persistently in VRAM, while offloading all peripheral tasks (Speech-to-Text, Text-to-Speech, Wake Word detection, Screen Capture) to the Ryzen CPU using highly optimized instruction sets.

---

### **Target Architectural Layout**

```
 [ Microphone ]        [ Wayland Screen Capture ]
       │                           │
       ▼ (Wake Word Trigger)       ▼ (Silent Overwrite Loop)
┌──────────────┐             ┌──────────────────────────┐
│ openWakeWord │             │ grim / gnome-screenshot  │
└──────┬───────┘             └─────────────┬────────────┘
       │                                   │
       ▼                                   │
┌──────────────────────────┐               │
│  faster-whisper (CPU)    │               │
└──────┬───────────────────┘               │
       │ (Text Transcript)                 │ (/tmp/screen.jpg)
       └───────────────┐   ┌───────────────┘
                       ▼   ▼
             ┌──────────────────────────┐
             │  Python Orchestrator     │
             └─────────┬────────────────┘
                       │ (Combined JSON Payload)
                       ▼
             ┌──────────────────────────┐
             │   Ollama Engine (GPU)    │
             │   → Qwen2.5-VL (3B)      │
             └─────────┬────────────────┘
                       │ (Text Stream Output)
                       ▼
             ┌──────────────────────────┐
             │  Piper TTS / Kokoro-82M  │
             └─────────┬────────────────┘
                       ▼
                 [ Speakers ]

```

#### **Component Allocation Blueprint**

1. **Central Brain (GPU - Pinned):** `Qwen2.5-VL (3B)` running via Ollama. It consumes roughly 2.2–2.5 GB of VRAM, leaving headroom for the context window and hybrid desktop rendering. It acts as a single-pass inference node that natively processes code parsing, math problems, or visual interface diagnostics without shifting models.
2. **Audio Ingest (CPU):** `faster-whisper` (tiny or base flavor). Utilizing the Ryzen CPU's AVX2 vectors guarantees a sub-500ms transcription phase without stepping on the GPU footprint.
3. **Vision Capture (Host OS Daemon):** A background loop writing to a volatile directory (`/tmp/screen.jpg`). Bypasses Wayland security sandboxing by running a native command (`grim` or `gnome-screenshot`) triggered via system orchestration.
4. **Audio Egress (CPU):** `Piper TTS` or `Kokoro-82M`. Converts streamed chunks back to verbal speech with negligible latency on the host CPU.

---

### **Operational Notes for Future Instances**

* **Gaming Toggle Script:** Before firing up a 3D gaming stack, the local environment must yield VRAM to avoid driver OOM crashes. Use a programmatic system execution toggle:
```bash
alias game-mode="ollama stop qwen2.5-vl:3b"

```


* **CachyOS Deployment Advantage:** When automating this setup on CachyOS, skip general `apt` dependencies. Build execution binaries using optimized compiler states available in the Arch User Repository (AUR) to extract maximum execution speed from the Ryzen 5 architecture.