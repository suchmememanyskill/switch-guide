# Launching CFW

Now that the preparation work is out of the way, we're finally ready to launch custom firmware on the Switch.

Unlike systems such as the DSi, Wii, or 3DS, Switch CFW is currently volatile. It will only work as long as your Switch is on. As soon as your Switch completely loses power for any reason (shutting down, battery dying, etc.), CFW will no longer be active and you will need to follow these instructions again.

!!! danger "Keep emuMMC offline at all times"
    Your emuMMC (emuNAND) should never connect to Nintendo. For online play, eShop browsing, or any other Nintendo online activity, use your sysNAND. Using both emuMMC and sysNAND online will likely result in a ban.

=== "Instructions for emuMMC"

    #### Instructions:

    1. From Hekate's `Home` menu, navigate to the `Launch` menu.
    2. Find `Atmosphere FSS0 EmuMMC` and launch it.

    Hekate is now booting into your emuMMC. To verify that your emuMMC launched properly, open System Settings and navigate to System. You should see `AMS` next to the version number (`AMS` indicating that you're booted into Atmosphere), as well as an `E` at the end (indicating you are booted into emuMMC).

    ![Atmosphere version string](img/launching_cfw_atmosphere_version_string2.jpg)

=== "Instructions for sysCFW"

    #### Instructions:

    1. From Hekate's `Home` menu, navigate to the `Launch` menu.
    2. Find `Atmosphere FSS0 sysMMC` and launch it.

    Hekate is now booting into sysCFW. To verify that sysCFW launched properly, open System Settings and navigate to System. You should see `AMS` next to the version number (`AMS` indicating that you're booted into Atmosphere), as well as an `S` at the end (indicating you are booted into sysCFW).

    - **Note:** You will also have the `Atmosphere FSS0 EmuMMC` launch option in Hekate, launching it will just result in an error and is expected because you don't have an emuMMC.

    ![Atmosphere version string](img/launching_cfw_atmosphere_version_string3.jpg)

!!! tip "Rebooting to Hekate"
    Once booted into CFW, you can easily get back to Hekate by holding the power button, and selecting `Restart` in the power menu or by using the "reboot to payload" homebrew app in the homebrew menu. (Note that while the Reboot to Payload *app* app does *not* work on modchipped Switch consoles, those already automatically run payloads upon reboot in the first place by default.)

-----

### **Launching the Homebrew Menu**

You will now be able to launch the Homebrew Menu by opening the album or by holding the R button while launching any game (including demos/cartridges), or application (e.g. YouTube/Hulu). If R is not held, the game or application will launch like normal.

!!! warning "A note about using the album for the Homebrew Menu"
    - Using Album for the Homebrew Menu instead of a game or application has several limitations, including but not limited to: a smaller amount of available memory (RAM), as well as being unable to launch a full-featured web browser. It is strongly recommended to launch homebrew through applications or games instead.


### **About the included Homebrew apps**

See the [Homebrew](/homebrew/) tab for information about what the included Homebrew apps do.

If you wish to install more homebrew apps, place them (`.nro` files) in the `switch` folder on your microSD card.

-----

### **Installing Android/Linux**

If you've partitioned your microSD card for preparation of Android/Linux earlier, you can continue with the installation of Android/Linux here with the guides below:

[Android installation guide :material-arrow-right:](../../extras/installing_android.md){ .md-button .md-button--primary } [Linux installation guide :material-arrow-right:](../../extras/installing_linux.md){ .md-button .md-button--primary }

??? "Frequently Asked Questions about this page"
      - **Q: How can you verify that sysCFW / emuMMC launched properly?** <br>
          A: Once you boot into the Switch's HOME Menu, navigate to Settings > System. The system version should be prefixed with an S or E, standing for SysMMC or EmuMMC respectively. Seeing either of these confirms which environment you are using.
      - **Q: What options do you have for rebooting to Hekate while booted into CFW?** <br>
          A: If you use a modchip, your console will automatically boot into whatever payload that your modchip would normally boot into via a coldboot, after clicking the restart button in the power-off menu. This can be any payload, but ideally is Hekate.
          If you use no modchip (and you're using a V1 console), your console will "reboot-to-payload" by default, triggering whatever fusee payload is located in `atmosphere/reboot_to_payload.bin`. This can be any payload, but ideally is Hekate.
      - **Q: Where can I find additional homebrew apps?** <br>
          A: One of the more convenient sources is the (Homebrew App Store)[https://github.com/fortheusers/hb-appstore/releases], hosted by (4TU)[https://gitlab.com/4TU]. You can also browse the (r/SwitchHacks)[https://www.reddit.com/r/SwitchHacks/] subreddit.
