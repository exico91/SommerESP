
## Instructions
You can buy here (soon) the kit that includes the two boards and a cable or you can build one yourself. You can find the BOM (bill of materials) [here](/Kicad/project/bom/ibom.html) and the gerber files [here](/Kicad/project/gerbers/). I used JLCPCB for my orders but there are also other manufactures.

### Installation
 1. Remove the plug from the wall, or cut off power to the Sommer garage door controller
 2. Write your firmware if you want or use it as is. You can find a basic yaml [here](/ESPHOME/esphome.yaml). To do so you will need a serial programmer and set it to 3.3V, connect GND, VIN, RX and TX to the controller board and power it on while pressing BOOT on the board. When you are done remove the serial programmer. DO NOT connect the programmer while the board is connected to the power board or inserted in the Sommer controller.
 3. Open the controller but pay attention to the keypad cable when you remove the cover
 4. Place the power board and the controller board as shown:
![](/pics/main.jpg)
 6. Connect the cable from the power board to the controller board
 7. Flip the first two switches to ON on the dip switch array on the Sommer controller
 8. Connect the keypad to the controller board in the same orientation as it was before
 9. Close the cover and power it on. You should be able to see a wifi network and connect to it to configure the module.

### Flashing and extra pins
To flash connect you serial programmer to the exposed pins on the controller board. DO NOT connect the programmer while the board is connected to the power board or inserted in the Sommer controller.
From top to bottom the pins are in this order:

GPIO05
GPIO03
3.3V
TX
RX
GND

Press BOOT while powering on the programmer to send the controller in flashing mode.

## Compatibility
This project should work with Sommer Base+ and Pro+.
The main focus of this project is ESPHome and Homeassistant but you can flash whatever you want on the ESP32-C3.
Check [here](/pinout.md) for the pinout.
 
 
## Origins
A thank you to https://github.com/jampez77/garage_door_sensor/ and https://github.com/azrael783/esphome_garagedoor_opener for giving me the ispiration to do this project, a lot of the code and core functionality is similar to these projects. Unfortunately neither did what I needed, cheap and invisible installation. Unfortunately the two Sommer modules (Conex and Output OC) are not cheap for what they are and using a DC-DC converter and relais externally is bulky and unsightly. I took the matter into my hands and now is almost plug and play and places where the two Sommer modules were.