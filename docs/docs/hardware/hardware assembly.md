# Hardware Assembly

## Qwiic Assembly

Since this is a Qwiic breakout, all we need to do is plug it into a Qwiic-comaptible development board, like the RedBoard IoT shown below, with a Qwiic cable. After that, plug the RedBoard into a computer over USB-C and we can move on to using the SparkFun BMA456 Arduino library to get data from the sensor:

![Photo of the BMA456 connected to RedBoard IoT - RP2350 via Qwiic](/img/QwiicBMA456-Assembly.jpg)

## Interrupt Assembly

All of the BMA456's feature engines use one or more of the interrupt pins on this breakout. When using those features like several of the following Arduino examples show, you'll want to connect INT1 and/or INT2 to an interrupt-capable pin on your microcontroller. The photo below shows INT1 connected to `D29` on the RedBoard IoT - RP2350:

![Interrupt pin and Qwiic assembly photo](/img/QwiicBMA456-Interrupt.jpg)