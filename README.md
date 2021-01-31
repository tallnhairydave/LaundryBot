# LaundryBot
ESP8266 based CT Clamp sensor for monitoring washing machine power usage and reporting into HomeAssistant

I've included the STL's to print out my housing for the circuit board that holds the Wemos D1 mini, the display, and the circuit to connect to the CT Clamp.

## BILL OF MATERIALS:
* 1 x Wemos D1 Mini ESP8266 
* 1 x 1.3inch I2C Serial 128x64 SSH1106 OLED LCD Display  
* 1 x 4 pin female header for solderable protoboard for the display
* 2 x 8 pin female header for solderable protoboard for the D1 Mini (my board came with these)
* 2 x 8 pin male headers for the D1 mini (my board came with these and I just had to solder them on)
* 1 x 30A 0-1V output CT Clamp, e.g. https://www.amazon.co.uk/gp/product/B07MY361ZW - Important note, your CT clamp MUST have an inbuilt "burden resistor" as my circuit used (see the fritzing diagram) does include one, as the CT Clamp I used has a burden resistor built in. When I cut off the 3.5mm headphone jack from my CT Clamp, I found it had one red core and one black core. I connected these to the 2 wire terminal block as shown in the fritzing diagram.
* 1 x Electrocookie 1/2 size solderable breadboard, or Adafruit 1/2 size protoboard. Both will fit in the case as they have the same 3mm fixing holes.
* 1 x 90 degree micro USB cable (if you want the power for the D1 mini to exit downwards from the case)
* 2 x M3x6 (no longer than M3x8) machine screws to hold the protoboard in the case
* 1 x 10µF Capacitor
* 2 x 10k Resistors
* 1 x 2 wires screw terminal for solderable protoboard (note that the terminal block I used occupies 3 pins width on the board, with an unused column between it's two pins, see the fritzing diagram)
* 2 x M2.5x8 machine screws to hold the display to it's printed support. I designed the support to have M3 screw holes, but they printed too small so had to use M2.5 screws instead. YMMV
* A small piece of 1mm thick foam tape (e.g. 3M VHB) to stick the base of the screen support piece to the protoboard if desired.
* Assorted 22 AWG wires to make jumpers for the solderable protoboard
* Assorted heatshrink tube (a) to tidy the wiring loom for the display, and (b) to insulate the soldered joint between the CT Clamp to two pairs of the CAT6 cable used to extend the wiring. 

