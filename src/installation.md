# Installing Sine

There are two ways to install Sine, automatically and manually. The automatic method involves an installer that does all the heavy-lifting, where as the manual method lets you do it all yourself.

### Automatic
To install Sine automatically, go to the [releases page](https://github.com/CosmoCreeper/Sine/releases/) of Sine, and find the version that you want to install. Then, under the assets section for that release, find the appopriate installer for your OS (Windows, Mac, and Linux) and CPU architecture (x86 and ARM). Once you've found the appropriate one, click and download it. Then, you may follow the provided guides for each operating system listed below.

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

### Manual
> Please note that this guide only works on Sine v2.3 and above.

1. **Locate your browser's installation directory:**
    - Find the folder where your browser is installed on your system (e.g., C:\Program Files\{browser_name}\ on Windows).

2. **Set up Sine's bootloader:**
    - Download ```program.zip``` and ```profile.zip``` from the [releases page](https://github.com/sineorg/bootloader/releases/) of the bootloader's repository. Ensure that whichever release you choose to download it from, that it supports the Sine version you're trying to download (listed at the top of the release description).
    - Extract ```program.zip``` into the root of your browser's installation directory (merging and replacing files if required).

3. **Configure your browser's profile:**
    - Open your browser and go to ```about:support``` in the address bar.
    - In the table, find ```Profile Folder``` and click ```Open Folder``` to access your current profile directory.
    - Inside the profile folder, navigate to the chrome directory (create it if it doesn’t exist).
    - Extract ```profile.zip``` from step 2 into the root of this folder.
    - Now, go to the [releases page](https://github.com/CosmoCreeper/Sine/releases/) of Sine and download ```engine.zip```.
    - Extract ```engine.zip``` into the newly-added JS folder (inside of your chrome folder).

5. **Clear your browser’s startup cache:**
    - Return to ```about:support``` in your browser.
    - Click the ```Clear Startup Cache``` button in the top-right corner.

6. **Restart your browser:** Close and reopen the browser to apply the changes.
