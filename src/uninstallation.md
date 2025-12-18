# Uninstalling Sine
Sine may be uninstalled using one of two ways, the auto-installer method, or manually.

### Automatic
To uninstall Sine automatically, go to the [releases page](https://github.com/CosmoCreeper/Sine/releases/) of Sine, and find the version that you want to uninstall (it typically doesn't matter, but just in case, match it up with your version). Then, under the assets section for that release, find the appopriate installer for your OS (Windows, Mac, and Linux) and CPU architecture (x86 and ARM). Once you've found the appropriate one, click and download it. Then, you may follow the provided guides for each operating system listed below.

- **Windows:** Execute the downloaded file.
- **Mac:** For Mac, you have to unquarantine the file, give it binary permissions, and then execute it. To do so, open the terminal in the location of the installer and then run the following commands (replace sine-osx-arm64 with sine-osx-x64 if you use x64):
  ```
  xattr -d com.apple.quarantine ./sine-osx-arm64
  chmod +x ./sine-osx-arm64
  sudo codesign --force --deep --sign - sine-osx-arm64
  ./sine-osx-arm64
  ```

- **Linux:** For Linux, you just have to give it binary permissions, and then execute it. To do so, open the terminal in the location of the installer and then run the following commands (replace sine-linux-x64 with sine-linux-arm64 if you use ARM):
  ```
  chmod +x ./sine-linux-x64
  ./sine-linux-x64
  ```

Once the installer is open, fill out all the details, and when it asks you if you want to install or uninstall Sine, pick uninstall.

### Manual
> Please note that this guide only works on Sine v2.3 and above.

1. **Remove Sine from your browser's installation directory:**
    - Find the folder where your browser is installed on your system (e.g., C:\Program Files\{browser_name}\ on Windows).
    - Delete ```config.js``` from that folder.
    - Navigate to ```defaults/pref/```, and delete ```config-prefs.js```.

3. **Configure your browser's profile:**
    - Open your browser and go to ```about:support``` in the address bar.
    - In the table, find ```Profile Folder``` and click ```Open Folder``` to access your current profile directory.
    - Inside the profile folder, navigate to the chrome directory.
    - Delete folders named ```JS```, ```sine-mods```, and ```utils```.

5. **Clear your browser’s startup cache:**
    - Return to ```about:support``` in your browser.
    - Click the ```Clear Startup Cache``` button in the top-right corner.

6. **Restart your browser:** Close and reopen the browser to fully remove Sine.
