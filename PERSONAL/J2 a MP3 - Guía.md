## Step 1: Prep and Clean the Phone

1. **Factory Reset:** Go to **Settings > General management > Reset > Factory data reset**. This wipes all old files and clears the limited storage.
    
2. **Turn on Airplane Mode:** Drop the notification bar and turn on Airplane Mode. Leave it on permanently to kill the cellular radios and save battery.
    
3. **Turn on Bluetooth:** Manually turn Bluetooth back on so you can connect wireless headphones.
    

---

## Step 2: Install Your Music App

Before locking down the system, install the app you plan to use.

- **Option A:** Download the official **Rockbox APK** via the phone's browser (you must enable "Install from Unknown Sources" in Settings).
    
- **Option B (Recommended):** Download **Musicolet** from the Play Store. It is lightweight, 100% offline, and works much better on touchscreens than the Rockbox port.
    

---

## Step 3: Strip Android to the Core (Optional)

To remove the Phone dialer, SMS, browser, and background bloatware so the phone _only_ plays music:

1. Go to **Settings > About phone** and tap **Build number** 7 times.
    
2. Go back to **Developer options** and turn on **USB Debugging**.
    
3. Plug the phone into a PC and use a free tool like **ADB AppControl**.
    
4. Uninstall the bloated apps, but **do not** delete any system Bluetooth files (`com.android.bluetooth`) or the core System UI.
    

---

## Step 4: Lock the Interface (Pick ONE Method)

Choose how you want to hide the rest of Android and block the top swipe-down menu:

### Method A: Screen Pinning (The Easiest Way)

- Uses native Android settings. No extra apps required.
    

1. Go to **Settings > Security > Screen pinning** and turn it **On**.
    
2. Open your music app.
    
3. Press the **Recent Apps** (Square) button, swipe up on the music app card, and tap the **Pin icon**.
    
4. _Result:_ The phone is trapped in the app, and the top pull-down menu is automatically blocked.
    

### Method B: Kiosk Launcher (The Permanent Way)

- Replaces the phone's desktop entirely.
    

1. Download a kiosk app (like **Fully Kiosk** or **Kiosk Launcher**) from the Play Store.
    
2. Go to **Settings > Apps > Default apps > Home app** and set the Kiosk app as your default home screen.
    
3. Open the Kiosk settings, allow _only_ your music app to run, and turn on the **"Disable Status Bar / Notification Shade"** toggle.
    

---

## Step 5: Transfer Your Music

1. Connect the phone to your PC via a USB cable.
    
2. Select **File Transfer / MTP** mode on the phone screen.
    
3. Drag and drop your MP3 files into the phone's internal `Music` folder (or onto a MicroSD card).
    
4. Open your music app, let it scan the files, and you're good to go.
    

> **Note:** If you need to pair new Bluetooth headphones in the future, you will have to temporarily unpin the screen or exit Kiosk mode to access the main Android Bluetooth settings.