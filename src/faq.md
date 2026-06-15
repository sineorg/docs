# Frequently Asked Questions (FAQ)

### Why is installation failing on Linux?

Since Linux varies heavily in how your browser and OS can be installed, we recommend verifying the following.

- The `unzip` tool is installed in my terminal, and is added to PATH. (Not in documentation as this requirement will be removed soon.)
- The browser path I am passing to the installer exists.
- I am selecting a used profile when prompted. (I am not clicking on "Show unused profiles" and clicking one of them)
- I am not passing the path to my browser binary to the installer, but rather a directory that contains not only the binary, but a folder named `defaults` too.
- I am not attempting to install Sine into flatpak with the auto-installer. (should be done manually or via `sine-flatpak.sh` from an old version of Sine)

If you have verified all of the above and installation still fails, please request help on [our Discord](https://discord.gg/P76BvB2MXS).

### Why is installation failing on macOS?

Since macOS has special requirements, we recommend verifying the following to determine why Sine is failing to install.

- I have enabled Full Disk Access for the macOS terminal.
- The browser path I am passing to the installer exists.
- I am selecting a used profile when prompted. (I am not clicking on "Show unused profiles" and clicking one of them)
- I have removed the quarantine flag for the installer using `xattr`.
- I have followed all of the commands listed in the installation documentation exactly.

If you have verified all of the above and installation still fails, please request help on [our Discord](https://discord.gg/P76BvB2MXS).

### Why does my antivirus block Sine's installer on Windows?

**This is a stub.**

Please view more details at https://github.com/CosmoCreeper/Sine/issues/506.

### What data does Sine collect?

**This is a stub.**

We do not voluntarily collect any telemetry.
