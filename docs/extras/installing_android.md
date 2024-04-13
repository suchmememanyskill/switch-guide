# Installing Android

!!! warning "Have you partitioned your microSD card?"
    This guide assumes that you've followed the NH-Server guide up until this point, your microSD card should be partitioned accordingly. If you didn't do so, see [this page](/user_guide/all/partitioning_sd_syscfw) of our guide or the bottom of this page for instructions on how to solely install Android on the official Switchroot Wiki.

This page will detail the setup of the latest release of Switchroot Android, Android 11, for your Nintendo Switch. This page assumes that you have no previous installation, so please do not follow this if you already have Switchroot Android installed on your microSD card, as it will overwrite your data. This page will not detail things such as rooting and overclocking; links to these types of additions can be found in the [Power User Guides](#power-user-guides) section at the bottom of this page.

!!! info "Looking for Android 10?"
    An unfortunate bug with clocking on Android 11 results in degraded performance for Erista (v1) units on Android 11. Android 10 installation is not covered here, but there is a [guide](https://wiki.switchroot.org/wiki/android/10-q-setup-guide) on the Switchroot Wiki. However, Android 11 is the currently supported version and uses much more recent graphics drivers, etc.

### **Requirements:**
- A Nintendo Switch console that is capable of running Hekate. <br>
- A microSD card *larger than* 8GB.
    - Please consult the [Switchroot microSD Card Guide](https://wiki.switchroot.org/wiki/sd-card-guide) before buying!
- A good quality, data-transfer capable USB-A to USB-C cable.
    - C-to-C is very glitchy and will be fixed in next release.
- A computer.

### **Instructions:**

#### Step 0: Prepare Necessary State

If you have official Joy-Cons, you can set up auto-pairing so undocking them automatically connects to Android without having to re-pair between HOS and Android. To make this work, boot HOS, ensure both work undocked (pair them), and reboot to Hekate. Select `Nyx Options` followed by `Dump Joy-Con BT`. You should see "Found 2 out of 2 Joy-Con pairing data!"

!!! tip "Have a Switch Lite?"
    You should poke the dump button in Hekate anyway--this will dump factory stick and IMU calibration for use in Android.

-----
    
#### Step 1: Downloading Files

Download the latest `.7z` release archive from [the official Switchroot download site](https://download.switchroot.org/android-11/)--choose `nx-atv...` for Android TV (more controller- and dock-optimized experience) or `nx-tab...` for standard Android (a more standard Android tablet experience). Both are usable with controllers and docking, but only tab supports proper touch input.

!!! tip "If you prefer [TWRP recovery](https://twrp.me/)..."
    ...you can download `twrp.img` from the [extras folder](https://download.switchroot.org/android-11/extras/).

-----
    
#### Step 2: Arranging the microSD Card

!!! tip "Are you using a normal model V1 or V2 Switch?"
    These models have a poorly designed microSD card reader and repeated removals/reinsertions can cause the reader to fail over time. Please use Hekate SD UMS to transfer files instead of removing the microSD card from your Switch!
    
    - This can be done by booting into Hekate and going to `Tools` > `USB Tools` > `SD Card` and plugging your Switch into your PC via USB.

Extract the archive to the root of the microSD card (the FAT32 partition). The microSD card file structure should look more or less like this:

```
root
|- bootloader
|  |- ini
|  |  |- ...
|  |- payloads
|  |  |- ...
|  |- res
|  |  |- ...
|  |- sys
|  |  |- ...
|- Nintendo (if you use stock)
|  |- ...
|- switchroot
|  |- android
|  |  |- ...
|  |- install
|  |  |- ...
|- lineage-18.1-[date]-UNOFFICIAL-[device].zip
```

!!! tip "If you downloaded TWRP..."
    ...you have to replace `/switchroot/install/recovery.img` with `twrp.img`. No need to rename the file, just swap it out.

-----
    
#### Step 3: Flashing Android

Open the Hekate partition manager (located in `Tools` > `Partition SD Card`) and select Flash Android at the bottom of your screen. All three images should be found and successfully flashed. Select the option to reboot to recovery.

Once in recovery, select `Factory Reset` followed by `Format Data`. This *does not delete anything here*, but rather is used to prepare your data partitions for flashing. Ignore any errors that may appear. Return to the main menu and select `Apply Update` followed by `Select from SWITCH SD`. Find and select the `lineage-18.1...` zip in the list, and wait for it to finish.

!!! warning "Did the zip fail to flash?"
    Your microSD card is likely bad. Take a look at Hekate's microSD card info and consider buying a better card.

!!! tip "If you are using TWRP..."
    ...good luck. TWRP is for advanced users only and no support will be provided. The image is provided for power users.

Once done, reboot the system when prompted--Android is now installed.

### **Post-Install**

#### Tips and Tricks

- If Joy-Con autopairing has not kicked in, try a reboot. Sometimes the first boot doesn't pick up the addition.

- To access recovery/TWRP: hold `VOL+` on reboot.

- To access Hekate from Android: hold `VOL-` on reboot.

- To reboot back to Android: hold `Power` for a few seconds and perform a standard reboot.

- To return to stock firmware (`OFW`): power your Switch off and on normally.

#### Power User Guides

To learn more about using the Switch Configuration App and overclocking, see the [Switch Configuration App](https://wiki.switchroot.org/wiki/android/11-r-setup-guide#switch-configuration-app) section. Furthermore, you can check out the [INI guide](https://wiki.switchroot.org/wiki/android/11-r-ini-guide) as well.

### **Need Help?**

Join the [Switchroot Discord server](https://discord.gg/N9PPYXjWMY).

### **Official Switchroot Documentation**

If you wish to solely install Android to your microSD card, see the [official Switchroot Wiki guide](https://wiki.switchroot.org/wiki/android/11-r-setup-guide). Make sure you back up the data on your microSD card beforehand (as is also mentioned during the official guide).

-----

This page was made in collaboration with `makinbacon21` on Discord. See the collapsible section below for the Switchroot guide maintainers.

??? note "Switchroot Project Staff (Android / Linux)"
    If you'd like, you can donate to the people who made this project possible using these links.

    - makinbacon (Android developer)
    [https://paypal.me/makinbacon21](https://paypal.me/makinbacon21)

    - npjohnson (Android developer)
    [https://paypal.me/nolenjohnson](https://paypal.me/nolenjohnson)

    - CTCaer (Linux & Low level developer, Hekate maintainer)
    [https://www.patreon.com/ctcaer](https://www.patreon.com/ctcaer)

    - ave (Infrastructure & Hosting)
    [https://patreon.com/aveao](https://patreon.com/aveao)
