# Lenovo TB8504X
**This repository contains all the links and files for custom rom installation on lenovo tab TB8504X including ome unlocking with there original source links, if source links are not found or working its will contains files that were downloaded from original source, All credit goes to there respectful owner/creators this repositor just created in sense to collected all the information in one place**

# Disclaimer

**The files and information provided for the Lenovo TB8504X are distributed strictly as-is and have not been modified by me in any way. All files are presented exactly as obtained from their original sources, and no warranties or guarantees of any kind are provided regarding their accuracy, reliability, or functionality.**
**I hereby disclaim all liability for any direct, indirect, incidental, consequential, or special damages, including but not limited to data loss, device malfunction, or hardware damage, arising from the use, misuse, or inability to use these files or any related instructions.**

**By accessing or using these files, you acknowledge and agree that:**

**1.You are using them entirely at your own risk.**\
**2.I bear no responsibility for any outcomes resulting from their use.**\
**3.You waive any and all claims, legal or otherwise, against me related to these files and instructions.**

**If you do not agree with these terms, do not use or download any files provided.**


# lets begin
Here are general instructions for unlocking the OEM bootloader of the Lenovo TB8504X. Proceed at your own risk—unlocking the bootloader may void your warranty and can lead to data loss or even device malfunction. Follow the steps carefully:

Step 1: Backup Your Data\
1.Unlocking the bootloader will wipe all data on your device.\
2.Backup important files, photos, and settings before proceeding.

Step 2: Enable Developer Options\
1.Go to Settings > About Tablet.\
2.Scroll down and tap Build Number 7 times until you see "You are now a developer!"

Step 3: Enable OEM Unlocking and USB Debugging\
1.Go to Settings > System > Developer Options.\
2.Enable OEM Unlocking (toggle it on).\
3.Enable USB Debugging.

Step 4: Install ADB and Fastboot Tools on Your PC\
1.Download and install Android SDK Platform Tools from the official Android developer website.\
~~~ bash
https://developer.android.com/tools/releases/platform-tools
~~~
2.Extract and install the tools on your PC.

Step 5: Connect the Device to PC\
1.Use a USB cable to connect your Lenovo TB8504X to the computer.\
2.Open a Command Prompt/Terminal in the folder where ADB and Fastboot are installed.\
Enter the following command:\
```bash
adb devices
```
If your device is detected, you will see its serial number.

Step 6: Boot into Fastboot Mode\
Reboot the device into Fastboot mode by running:\
Copy code\
```bash
adb reboot bootloader
```
Alternatively, power off the device and press Volume Down + Power Button simultaneously until the Fastboot screen appears.

Step 7: Unlock the Bootloader\
Enter the following command:\
Copy code\
```bash
fastboot oem unlock
```
Confirm the unlocking process on your device using the Volume Keys to navigate and Power Button to confirm.

Step 8: Reboot the Device\
Once the bootloader is unlocked, reboot the device using:\
Copy code\
```bash
fastboot reboot
```
The device may take longer to boot during the first startup after unlocking.

Important Notes:\
Unlocking the bootloader voids the warranty.\
It will erase all data on the device.\
Ensure your device has at least 50% battery before starting.\
Make sure to install proper USB drivers for Lenovo devices if the device is not detected.\
Proceed only if you understand the risks involved.

