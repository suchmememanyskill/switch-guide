### **Information**

sys-clk is a [sysmodule](../../homebrew#terminologies) that allows you to overclock the hardware of your Switch. The usage, configuration and clock speed information can be found on the official Github repository [here](https://github.com/retronx-team/sys-clk)

!!! danger "Limits of sys-clk"
    sys-clk has limits for a reason, which is to not damage the hardware of your Switch. Using ***any*** modified version of sys-clk puts your Switch at risk of hardware failure. We do not support any modified version of sys-clk nor should you ever touch them. Overclocking is not something you should be doing 24/7 as overclocking in general will always degrade/wear out the hardware of your Switch faster and you should know what you're doing if you *do* decide to do so.

-----

#### Installation requirements:
- An archive manager like [7-Zip](https://www.7-zip.org/)
- The latest release of [sys-clk](https://github.com/retronx-team/sys-clk/releases) (the `sys-clk-(version).zip` file)

#### Installation instructions:
1. Boot into Hekate and go to `Tools` > `USB Tools` > `SD Card`, then plug your Switch into your PC via USB.
2. Your microSD card should now be accessible on your PC, open it.
3. Extract the `.zip` file to a location on your computer.
    - If your archive manager allows for it, you can also simply open the `.zip` file directly.
4. Copy the *contents* of the (extracted) `.zip` file to the root of your microSD card.
    - **Optional:** You can verify if you've installed sys-clk correctly, you should have a folder called `00FF0000636C6BFF` (sys-clk) in `sd:/atmosphere/contents`.
5. Boot into CFW.

-----

### **Basic usage instructions**

Open the Homebrew menu and open sys-clk's manager app. This app allows you to change the global clock speeds or clock speeds based on title.

-----

### **Troubleshooting**
#### **My Switch crashes on boot after I installed sys-clk!:**

**Cause:** If your Switch crashes on boot, make sure you're using the latest release of sys-clk. If it continues to crash afterwards, see the troubleshooting step at the bottom of this page.

&nbsp;

#### **My Switch crashes while using sys-clk!:**

**Cause:** You're either using a modified version of sys-clk and pushing the hardware of your Switch too far or your console is overheating. The cooling system of the Switch is *not* the best and overheating can be a cause of dried up thermal paste/lack of thermal paste. Overclock with caution and be careful, monitor the temperatures of your Switch using a Tesla-Menu overlay like [Status-Monitor-Overlay](https://github.com/masagrator/Status-Monitor-Overlay) (requires Tesla-Menu).

&nbsp;

#### **sys-clk isn't working!:**

Assuming you've followed the installation structions successfully, this is probably due to the archive bit being set on one or more folders/files on your microSD card. This is usually the result of copying files to a microSD card via a Mac. If you are experiencing this issue, try running the archive bit fixer utility via Hekate for all files.

This can be done by booting into Hekate and going to `Tools` > `Arch bit • RCM Touch • Pkg1/2` > `Fix Archive Bit`.
