Since you are using the `touchdesigner-linux` AUR package (the automated environment manager by Iswad), your TouchDesigner instance is running via a specialized Wine prefix.

  

Here is how MediaPipe interacts with that specific setup:

  

### 1. Direct Python Installation (Possible, but runs on CPU)

The `touchdesigner-linux` AUR package includes a built-in wrapper to install Windows Python wheels directly into your TouchDesigner prefix. You can install MediaPipe directly by running this in your Linux terminal:

  

Bash

```
td-install --pip install mediapipe opencv-python
```

**The Catch:**

While this allows you to write a Python Script TOP/CHOP inside TouchDesigner to process MediaPipe, it will run entirely through Wine's translation layer. You will likely lose GPU acceleration (MediaPipe relies heavily on Windows Media Foundation/CUDA which Wine struggles with), and grabbing your webcam through Wine's DirectShow wrapper (`/dev/video0` translated to a Windows device) can introduce latency. It will work, but it will be CPU-heavy.

  

### 2. WebBrowser TOP Plugins (Not Recommended)

If you are trying to use popular community `.tox` files (like Torin Blankensmith's) that rely on the **WebBrowser TOP** to run MediaPipe in JavaScript, you will likely run into crashes. The Chromium Embedded Framework (CEF) used by the WebBrowser TOP is notoriously buggy inside Wine, and passing webcam streams into it often fails or causes heavy graphical glitches.

  

### 3. The Best Workflow: Native Linux + OSC

Even with the AUR package, the most performant method is to run MediaPipe natively on your Linux host and send the data into TouchDesigner.

  

1. **Install MediaPipe natively:** Install it in your standard Arch Linux environment (`sudo pacman -S python-opencv` and `pip install mediapipe`).
    
      
    
2. **Process on the Host:** Write a small Python script that captures your webcam natively (using V4L2) and processes the landmarks.
    
      
    
3. **Send to TD:** Have the script send the coordinates to `localhost:7000` via OSC.
    
      
    
4. **Receive in TD:** Open TouchDesigner (via your AUR launcher) and drop an **OSC In CHOP** to catch the data.
    
      
    

This completely bypasses Wine for the heavy computer vision lifting, allows MediaPipe to access native Linux hardware acceleration, and leaves TouchDesigner free to just handle the rendering.