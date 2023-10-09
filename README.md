# SommerESP
A plug and play ESP32-C3 board to control Sommer garage doors

This combo is designed to replace the Sommer Conex Module and the Sommer Output OC Module.

The Sommer Conex Module is designed to replicate the press of the buttons on the controller of the garage door and the Sommer Output OC just provide the signal for the status and 24 Volts DC.

This prohect takes the 24V and converts it to 3.3V for the ESP32-C3 module, the DC regulator on the power board can take from 4.5V to 40V and cleanly output 3.3V then transfer it to the ESP board along with the status signal.

The ESP controller simulate the press of the buttons using a couple of optocouplers, simple enough. You can also attach other things to this board, i left a couple of GPIOS on pins along with the serial connection required to flash the module.

