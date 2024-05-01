### **Information**

SysDVR is a [sysmodule](../../homebrew#terminologies) that allows you to stream the screen of your Switch (while in-game/in an application) to your PC via the network or USB. Usage, configuration
and extensive troubleshooting information can be found on the SysDVR Wiki [here](https://github.com/exelix11/SysDVR/wiki).

-----

#### Installation requirements:
- An archive manager like [7-Zip](https://www.7-zip.org/)
- The latest release of [SysDVR](https://github.com/exelix11/SysDVR/releases) (the `SysDVR.zip` file)

#### Installation instructions:
1. Boot into Hekate and go to `Tools` > `USB Tools` > `SD Card`, then plug your Switch into your PC via USB.
2. Your microSD card should now be accessible on your PC, open it.
3. Extract the `.zip` file to a location on your computer.
    - If your archive manager allows for it, you can also simply open the `.zip` file directly.
4. Copy the *contents* of the (extracted) `.zip` file to the root of your microSD card.
    - **Optional:** You can verify if you've installed SysDVR correctly, you should have a folder called `00FF0000A53BB665` (SysDVR) in `sd:/atmosphere/contents`.
5. Boot into CFW.

-----

### **Troubleshooting**
#### **My Switch crashes on boot after I installed SysDVR!:**

**Cause:** If your Switch crashes with Error `2168-0002 (0x4a8)` and Title ID `00FF0000A53BB665`, you're using a version of SysDVR that's incompatible with your Switch firmware version and/or Atmosphere version. Update SysDVR and try again.

#### **My Switch crashes after I launch a game with SysDVR enabled!:**

**Cause:** If your Switch crashes with Error `2168-0002 (0x4a8)` and Title ID `00FF0000A53BB665`, you're using a version of SysDVR that's incompatible with your Switch firmware version and/or Atmosphere version. Update your SysDVR patches and SysDVR itself, then try again.

&nbsp;

#### **SysDVR isn't working!:**

Assuming you've followed the installation structions successfully, this is probably due to the archive bit being set on one or more folders/files on your microSD card. This is usually the result of copying files to a microSD card via a Mac. If you are experiencing this issue, try running the archive bit fixer utility via Hekate for all files.

This can be done by booting into Hekate and going to `Tools` > `Arch bit • RCM Touch • Pkg1/2` > `Fix Archive Bit`.
