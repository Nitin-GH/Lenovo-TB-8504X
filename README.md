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
**Here are general instructions for unlocking the OEM bootloader of the Lenovo TB8504X. Proceed at your own risk—unlocking the bootloader may void your warranty and can lead to data loss or even device malfunction. Follow the steps carefully:**

# Step 1: Backup Your Data
**1. Unlocking the bootloader will wipe all data on your device.**\
**2. Backup important files, photos, and settings before proceeding.**

# Step 2: Enable Developer Options
**1. Go to Settings > About Tablet.**\
**2. Scroll down and tap Build Number 7 times until you see "You are now a developer!**"

# Step 3: Enable OEM Unlocking and USB Debugging
**1. Go to Settings > System > Developer Options.**\
**2. Enable OEM Unlocking (toggle it on).**\
**3. Enable USB Debugging.**\
![oem-unlock-lollipop-1200x822](https://github.com/user-attachments/assets/4224d8cd-4435-4e20-becc-6b472016159d)



# Step 4: OEM unlocking is need in order to install custom roms on Lenovo-TB8504X for that you going to need few softwars
**Installation instruction are provided in websites so please pay attention to that we dont want to make this guide lengthy**\
**file 1.** https://qcomdriver.com/qualcomm-usb-driver-v1-0-10065-1 \
**file 2.** https://qdloader9008.com/qualcomm-qdloader-9008-driver-v1-00-25 \
**file 3.** https://qfiltool.com/qfil-tool-v2-0-3-5

# Note 
**You may encounter few errors regarding ports that's happen because your android drivers for adb are not setup properly, due to multiple reasons**
**if you not gettings fastboot device waiting errors (error 2) or sarah failed error (error 3) that most likely your port for port9008COM3 shwoing up but not connected or able to read adb drivers**

# **Error 1**
**Error 1 is the main error for most of the error this should not look like this**

 ![android error](https://github.com/user-attachments/assets/bb7ac249-6f55-4c4f-8d2d-98c861fbe31d)\
**Error 2**\
![fastboot error](https://github.com/user-attachments/assets/624bbe95-6d8c-441f-9761-ea0ea6a35bd6)\
**Error 3**\
![sarah failed](https://github.com/user-attachments/assets/2b735a61-cc37-4622-a20c-4d723be71bb4)\

**we will talk about error 2 more in later of the guide but i highly recommand the youtube video for error 1 and usb driver file is given in the video if that link fails you get that same version in this guide, its basically take from the video description link to keep it safe**

**Video** https://www.youtube.com/watch?v=5z1l6r9EDMo&ab_channel=TheTechipedia \
**I am not affiliated with any YouTuber or content creator.**

once that done we more to next step

# Step 5
# **1. open Qfil as admin**

![qfiladmin](https://github.com/user-attachments/assets/ee002de6-ba03-4620-9a13-4c081ef47aaa)\

# **2. Click Flat build(red arrow)**
![qfil arrow](https://github.com/user-attachments/assets/e2a0e7de-9946-4afd-98a3-a4422e21a5a2)\

# **3. browse your  then browse your prog_emmc_firehose_8917_ddr.mbn file**
![qfill arrow file](https://github.com/user-attachments/assets/4dbe3737-ee7d-4ba3-bcf2-2ae3384f6a07)

# **4. then click LOAD XML and choose RAW program upgrade**
![qfil arrow 2](https://github.com/user-attachments/assets/3d076ac7-5638-4088-80b4-aa1481d47dd8)

# **5. then choose patch file**
![qfill arrow 3](https://github.com/user-attachments/assets/5b199922-7a54-416f-baab-e5c47e267b24)

# **6. Now your Tab have to go into ELD mode before connecting it to the pc**


# **7. There are two methods to go into ELD mode**

 **method 1. connect your Tab to pc and select fil tranfer mode if not done before in usb deubgging and then open adb command prompt and type**
   ~~~bash
   adb reboot edl
   ~~~

**method 2. turn off your tab once it done wait for 3 second and press Volume up key and hold it for 2 sec and connect your usb while holding volume up at same time and your red notification light pop up without**
**turning it on its mean you are in ELD mode**

# **8. once you are into ELD mode and Qfil ports pop up like, just select port which will be preselected if not just in case and hit DOWNLOAD**
![qfill arrow 4](https://github.com/user-attachments/assets/40712c59-07b6-4164-9675-b96eb56084c5)

# **9. once the download has done and if will show you download success then Disconnect your Tab and turn it on and set it up again and turn on usb debugging, oem unlock again**

# **10. now connect your phone and choose file transfer in MTP


# Step 6: Install ADB and Fastboot Tools on Your PC

**1.Download and install Android SDK Platform Tools from the official Android developer website.**\
https://developer.android.com/tools/releases/platform-tools \
**2.Extract and install the tools on your PC.**\
**3.Go into the extracted folder and press leftShift then Right click and open termnial**
![shiftplusrightclick](https://github.com/user-attachments/assets/bcd9502a-a4fe-4409-bfad-3939ef11a955)




# Step 7 : Connect the Device to PC

**1.Use a USB cable to connect your Lenovo TB8504X to the computer.**\
**2.Open a Command Prompt/Terminal in the folder where ADB and Fastboot files are.**\
**Enter the following command:**\
```bash
adb devices
```
**If your device is detected, you will see its serial number.**

# Step 8: Boot into Fastboot Mode

**Reboot the device into Fastboot mode by running:**\
**Copy code**
```bash
adb reboot bootloader
```
**Alternate, power off the device and press Volume Down + Power Button simultaneously until the Fastboot screen appears Your tab will boot to fastboot showing FastBoot text with broken android icon..**

# Step 9: Unlock the Bootloader

**Enter the following command:**\
**Copy code**\
```bash
fastboot oem unlock
```
**unlocking process on your device its will look like this**\

![oem unlocking](https://github.com/user-attachments/assets/3742c084-9701-497d-8a4c-076685d2184c)

**Once it done it will erase all the data on your device and you all to resetup it again before moving on to flasing recovery and rom**


# Step 10: Reboot the Device
**Once the bootloader is unlocked, reboot the device using:**\
**Copy code**
```bash
fastboot reboot
```
**The device may take longer to boot during the first startup after unlocking.**

# step 11: flash recovery 
**1. once you set it up again and turn on usb debugging again and oem unlock again if not pre toggle before**
**2.now open adb command prompts type**

**adb reboot bootloader**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"and hit enter."\
**fastboot devices**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"and hit enter. If your tab codename appears go to next steps."\
**fastboot flash recovery**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"and hit space and drag and drop twrp image file. press enter."\

and flash you recovery
Important Notes:\
Unlocking the bootloader voids the warranty.\
It will erase all data on the device.\
Ensure your device has at least 50% battery before starting.\
Make sure to install proper USB drivers for Lenovo devices if the device is not detected.\
Proceed only if you understand the risks involved.

