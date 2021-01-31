# LaundryBot
ESP8266 based CT Clamp sensor for monitoring washing machine power usage and reporting into HomeAssistant. 

You need ESPHome add-on installed and running in HomeAssistant. 

1. Create a new ESPHome node
1. Update the laundrybot.yaml to suit your OTA and API passwords set during creation of the new node, and your WIFI network settings.
1. Compile and upload the code to your D1 Mini via serial for the first time from ESPHome. Future updates can then be OTA.
1. Add the code in the my_configuration.yaml file here to your configuration.yaml 
1. Check your configuration.yaml is valid, then restart HA.

I've included the STL's to print out my housing for the circuit board that holds the Wemos D1 mini, the display, and the circuit to connect to the CT Clamp.

THIS IS DESIGNED AND BUILT TO WORK WITH A UK SINGLE PHASE 240V 3 CORE MAINS POWER CABLE, the CT Clamp goes around the LIVE core of the wire inside a junction box.

I am using it to monitor my washing machine, which has a 13A fuse. 

I've made an "extension lead" by cutting a 1 gang 5M extension cable in half, exposing the three cores and re-terminating them inside a junction box with screw down cable glands for cable entry. That way, the mains cable is safe and the CT clamp can be placed around the LIVE wire to enable current to be monitored.

**I AM IN NO WAY RESPONSIBLE FOR ANY ISSUES THAT MAY ARISE IF YOU BUILD THIS CIRCUIT AND WIRE UP ANYTHING TO IT. PROCEED AT YOUR OWN RISK**

## BILL OF MATERIALS:
* 1 x Wemos D1 Mini ESP8266 
* 1 x 1.3inch I2C Serial 128x64 SSH1106 OLED LCD Display  
* 1 x 4 pin female header for solderable protoboard for the display
* 2 x 8 pin female header for solderable protoboard for the D1 Mini (my board came with these)
* 2 x 8 pin male headers for the D1 mini (my board came with these and I just had to solder them on)
* 1 x 30A 0-1V output CT Clamp, e.g. https://www.amazon.co.uk/gp/product/B07MY361ZW - Important note, your CT clamp MUST have an inbuilt "burden resistor" as my circuit used (see the fritzing diagram) does include one, as the CT Clamp I used has a burden resistor built in. When I cut off the 3.5mm headphone jack from my CT Clamp, I found it had one red core and one black core. I connected these to the 2 wire terminal block as shown in the fritzing diagram. Make sure that you clamp it on the LIVE core inside the junction box with the ARROWS on the CT Clamp matching the direction of current flow. **NEVER ALLOW THE CT CLAMP TO OPERATE "OPEN CIRCUIT" i.e. do not connect it around the live wire and turn on the power, UNLESS the wires from the CT Clamp are connected to the terminals on the circuit board**
* 1 x Electrocookie 1/2 size solderable breadboard, or Adafruit 1/2 size protoboard. Both will fit in the case as they have the same 3mm fixing holes.
* 1 x 90 degree micro USB cable (if you want the power for the D1 mini to exit downwards from the case)
* 2 x M3x6 (no longer than M3x8) machine screws to hold the protoboard in the case
* 1 x 10µF Capacitor
* 2 x 10k Resistors
* 1 x 2 wires screw terminal for solderable protoboard (note that the terminal block I used occupies 3 pins width on the board, with an unused column between it's two pins, see the fritzing diagram)
* 2 x M2.5x8 machine screws to hold the display to it's printed support. I designed the support to have M3 screw holes, but they printed too small so had to use M2.5 screws instead. YMMV
* A length of CAT6 network cable to run from the laundrybot location to the location of your power enclosure to house the CT Clamp. I used CAT6 as I had some lying around. CAT5e will work fine.  You could simply cut the ends off of a suitable length ethernet cable and use that instead of using spare cable from a spool like I did. 
* A small piece of 1mm thick foam tape (e.g. 3M VHB) to stick the base of the screen support piece to the protoboard if desired.
* Assorted 22 AWG wires to make jumpers for the solderable protoboard
* Assorted heatshrink tube (a) to tidy the wiring loom for the display, (b) to insulate the soldered joint between the CT Clamp to two pairs of the CAT6 cable used to extend the wiring, and (c) as needed for the mains cable, depending on how you terminate it inside the junction box.
* 1 x zip tie to act as strain relief on the CAT6 cable where it enters the Laundrybot housing in case it somehow gets tugged. You can also hot-glue it down to the protoboard. 
1 x ABS junction box at large enough to house the CT clamp and the mains power cable. Mine was 15cm x 11cm x 7cm and was just about the right size.
1 x one-gang extension lead that is long enough to go from the washer's mains socket to the floor, and tuck under the cabinet next to the washer. I ended up using a 5m cable.
1 x cable termination method of your choice to join the mains cable back together inside the junction box
3 x cable glands for the junction box (i used 20mm screw down cable glands that I had spare).

## Wiring diagram for the protoboard
![wiring diagram](https://github.com/tallnhairydave/LaundryBot/blob/main/fritzing_diagram.png)


