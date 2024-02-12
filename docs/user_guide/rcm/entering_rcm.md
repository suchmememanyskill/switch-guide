# Entering RCM

As the Switch uses a Tegra X1 processor, it has a special recovery mode that is, in most scenarios, useless for the end-user. Fortunately, due to the fusee-gelee vulnerability, this special mode acts as our gateway into CFW.

There are several methods of entering RCM (**R**e**C**overy **M**ode). The most affordable of these require nothing more than common household items (not recommended), while the most reliable are very cheap ($5-10) and can be bought places like AliExpress or Amazon, they can also can be 3D printed.

!!! danger "Patched Switch"
    Note that patched units **can** enter RCM, but it is not possible to send a payload on those systems. Also note that RCM is a different recovery mode than the one accessed by holding Volume Up, Volume Down and powering on your console.

!!! note "Information about the methods below"
    The order of methods on this page is in the order of ease. The easiest to immediately accomplish are listed at the top, and the most advanced/difficult methods are at the bottom and should not be attempted by most people.
    **USING A PAPERCLIP OR TIN FOIL CAN/WILL DAMAGE YOUR CONSOLE, DO NOT DO THIS!**

### **Instructions:**

1. Power off the Switch and use one of the methods listed below to short the pins on the right Joy-Con rail.
2. Hold `Volume Up` and press the `Power` button once while holding `Volume Up`.
    - If your Switch displays the Nintendo logo and boots normally or immediately shuts down, you didn't successfully enter RCM and should try again. Otherwise, if your console did not turn on normally, and the screen remained black with no backlight, your Switch is in RCM.
3. Once your Switch is in RCM, you may remove the RCM jig (if applicable) and continue with the next page of the guide by clicking on the button at the bottom of this page.

=== "RCM Jig (Recommended and easiest for beginners)"
    
    Some jig designs use paperclips, inheriting the same risks as the Metal Bridge / Paperclip method and should not be done.

    Once you have successfully entered RCM, you can take the jig out of the joycon rail.

    This method is similar to the Metal Bridge / Paperclip method, but is more reliable and safer in many cases. Jigs hold a wire in place so the correct pins (10 and a ground) are shorted every time.

    The RCM Jig pictured below is the model we recommend to get, if you're buying your Jig from a webshop like Amazon or AliExpress.

    ![recommended_jig](../rcm/img/recommended_jig.jpg)
		
    In the case you plan to make you own jig, this image lays out the pads numbers on the console. Make sure your jig NEVER touches pin 4. Pin 4 provides 5v power to the Joycons, if connected to any other pin you will fry the console.

    ![switchjigs.com jigs](../rcm/img/entering_rcm_jig.jpg)

    ![Console Numbered Pads Refrence](../rcm/img/entering_rcm_pads_numbered.jpg)


=== "Soldered Joy-Con Pads - Physical RCM Button (Safest but not recommended for beginners)"

    This method requires opening your right Joy-Con, voiding its warranty. Not for the faint of heart.

    This method comes to us from the mind of `pbanj` on Discord. All pictures of this method in action were provided by him, with some supplementary images provided by `eip` on Discord.
	
    The goal of this method is to open the right handed Joy-Con to the point that you can reach the contact pads easily. This is similar to the previous method, however you will be soldering wires to pins 7 and 10 (shown below) and wiring them to the "Joycon release button" at the top back of the right hand Joycon.

    ![joycon numbered pads refrence](../rcm/img/entering_rcm_solder_numbered.jpg)

    In order to start this method you will want to take two lengths of wire, and wrap one end of each into a small circle.

    ![wire refrence](../rcm/img/entering_rcm_button_1.jpg)
		
	You will then want to take the circular end of one of the wires and add a small amount of solder, keeping it mostly flat (ONLY DO THIS TO ONE OF THE WIRES!). You will then glue this wire down to the below point on the Joycon release button. Make sure glue doesn't cover the top of the solder/wire as it will act as a contact point. Also, ensure that you leave enough space for the button to function correctly. Try pushing the button from the outside and observing its travel path so that you can see where and how you should safely glue the solder glob.

    ![Eip joycon button refrence](../rcm/img/entering_rcm_button_5.jpg)
		
    ![pbanj joycon button refrence](../rcm/img/entering_rcm_button_3.jpg)
		
    The first wire should now be in place as seen by the green circle below. The second wire does not need any solder, instead you will hold it in place using the screw as shown by the red circle in the picture below.

    ![pbanj joycon button refrence](../rcm/img/entering_rcm_button_6.jpg)

    Pressing the Joycon button in you should now notice the solder point you created making contact with the piece of metal held in by the screw. Once you have these elements in place you want to connect one wire to pad 7 and the other to pad 10 (it doesn't matter which is which). After that you have successfully created an RCM button on your Joycon. You will now need to hold down the Joycon release button when attempting to boot RCM.

    ![pbanj joycon button refrence](../rcm/img/entering_rcm_button_2.jpg)



=== "Soldered Joy-Con Pads - 7 & 10"

    This method requires opening your right Joy-Con, voiding its warranty. Not for the faint of heart.

    The goal of this method is to open the right handed Joy-Con to the point that you can reach the contact pads easily. This is similar to the previous method, however the goal is to solder pins 7 and 10 (shown below) together with a surface-mount 0805 10k resistor. Apart from using a physical switch/button, this is currently considered the safest method that involves soldering to pads.

    ![joycon numbered pads refrence](../rcm/img/entering_rcm_solder_numbered.jpg)

    Here is an example from stuckpixel#3421 on the ReSwitched Discord server.

    ![stuckpixel solder example](../rcm/img/entering_rcm_solder_710_stuckpixel.jpg)



=== "Soldered Joy-Con Pads - 9 & 10"

    This method will result in the right Joy-Con being detected as in wireless mode while attached to the Switch, and this method may result in the Joy-Con being permanently detected as wireless if you update the Joy-Con firmware while this mod is installed. In the latter case, fixing this requires opening up the Joy-Con and reseating the battery. It is recommended to solder pads 7 and 10 together with a resistor instead.

    This method requires opening your right Joy-Con, voiding its warranty. Not for the faint of heart.

    The goal of this method is to open the right handed Joy-Con to the point that you can reach the contact pads easily. This is similar to the previous method, however the goal is to solder pads 9 and 10 (seen below) together. This can either be done using a small wire, or directly bridging the pads with solder.

    ![joycon numbered pads refrence](../rcm/img/entering_rcm_solder_numbered.jpg)
	
    Here is an example from yami0666 on our Discord server.

    ![YyAoMmIi solder example](../rcm/img/entering_rcm_solder_910_yyaommii.jpg)


=== "Bent Joy-Con Pins (Not recommended)"

    This method will result in the right Joy-Con being detected as in wireless mode while attached to the Switch, and this method may result in the Joy-Con being permanently detected as wireless if you update the Joy-Con firmware while this mod is installed. In the latter case, fixing this requires opening up the Joy-Con and reseating the battery.

    This method requires opening your right Joy-Con, voiding its warranty. Not for the faint of heart.

    The goal of this method is to open the right handed Joy-Con to the point that you can reach the contact pads easily, and use a thin object such as a knife to gently bend pin 9 and 10 (shown below) slightly up and towards each other so they touch, shorting them.

    ![Joycon Pin Refrence](../rcm/img/enterting_rcm_pins_numbered.jpg)

    Here is an example from Sonlen#1414 on our Discord server.

    ![Sonlen example](../rcm/img/entering_rcm_bent_pins.jpg)


[Continue to Sending a Payload :material-arrow-right:](sending_payload.md){ .md-button .md-button--primary }