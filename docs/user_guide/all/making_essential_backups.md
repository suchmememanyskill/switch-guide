# Making Essential Backups and dumping your prod.keys

## Making a NAND Backup

!!! danger "Important"
	A NAND backup is crucial to have, it's a full backup of the internal storage of your Switch and can be used to restore the device to a working state in case of emergencies. **DO NOT SKIP THIS STEP**

	Once the backup is finished, **keep it somewhere safe.** The best backup is the one you have but never need, and the worst backup is the one you need but never made. To save space, it's recommended to compress the end-result with a `.zip` file or something similar.

	It's highly recommended that you use an SD card that is formatted to FAT32 and has at least 32 gigabytes of space free. This will still work on smaller cards, but it's not ideal.

### Instructions:

1. Enter RCM and inject the Hekate payload.
    - If you use a modchipped Switch, you can simply just turn your Switch on with the hekate payload renamed to `payload.bin` on the root of your SD. 
2. Use the touch screen to navigate to `Tools` and then `Backup eMMC`
3. Tap on `eMMC BOOT0 & BOOT1`
    - This should only take a few seconds, but if your SD card is very slow, it may take around a minute.
4. Tap on `Close` to continue, then tap on `eMMC RAW GPP`
    - This will take a long time. Expect it to take between 10 minutes to an hour (or more, if your SD card is very slow).
    - On FAT32 SD cards or cards that have less than 32 gigabytes of space available, the NAND will be split into 1 or 2 gigabyte parts.
       - Hekate will stop producing these parts when it runs out of space. When this happens, do the following:
       - Power off your system.
       - Insert your SD card into your PC.
       - Move all files from the `backup` folder on your SD card to a safe location on your PC.
       - Insert your SD card into your Switch.
       - Enter RCM again, inject Hekate again, and continue the backup by tapping on `Tools` > `Backup eMMC` > `eMMC RAW GPP`
       - Repeat the process until the NAND is completely dumped.
5. Go to the top right and press `Close` > `Home`
6. Navigate to `Tools` > `USB tools` > `SD card` and plug your switch into your PC via USB.
7. Copy the `backup` folder on your SD card to a safe location on your PC.

-----

## Getting your console's unique prod.keys

!!! danger "Important"
    These keys are critical to have. These keys are required to decrypt the content and partitions on the internal storage of your Switch.
    In an extreme emergency, they can be used in conjunction with your NAND backup and other tools to restore your console to a working state.

### Instructions:

1. Tap the `Payloads` option, then press Lockpick_RCM.bin.
2. If Lockpick_RCM asks you to select between SysNAND and EmuNAND, choose SysNAND by navigating with the volume buttons and pressing the power button. If not, continue with step 4.
3. Lockpick_RCM should now inform you that your keys have been saved to `/switch/prod.keys` on the SD card.
4. Press any button to return to the main menu.
5. Navigate to 'Reboot to hekate' with the volume buttons and select it with the power button.
6. Once in hekate, navigate to `Tools` > `USB tools` > `SD card` and plug your switch into your PC via USB.
7. Copy `prod.keys` from the `switch` folder on your SD card to a safe location on your PC (it is suggested to copy it to the same place that you copied your NAND backup to).
    
[Continue to Launching CFW :material-arrow-right:](launching_cfw.md){ .md-button .md-button--primary }
