# Hardware Overview

## BMA456 Tri-Axis Accelerometer

The BMA456 from Bosch Sensortech<sup>&copy;</sup> is a high-precision, ultra-low power 16-bit tri-axis acceleration sensor that draws only 150&micro;A in full operation and as low as 14&micro;A in low-power mode. The BMA456 has programmable measurement ranges of &plusmn;2/&plusmn;4/&plusmn;8/&plusmn;16 g capable of a measurement resolution as high as 0.06 mg (in &plusmn;2g range). The BMA456 improves on previous versions with a zero-g offset of &plusmn;20 mg, noise density of 120 &micro;g/&radic;Hz and a bandwidth range of 12.5 Hz to 1600 Hz in performance mode and 0.78 to 400Hz in low power mode.

The accelerometer has an embedded intelligence engine capable of detecting steps (both detection and counting), activity, tilt on wrist and single/double taps and trigger interrupt events when they are detected. The BMA456 also features a dedicated auxiliary interface that can read and store data from one attached compatible sensor. The BMA456 automatically reads this data and stores it in its data registers and FIFO. Refer to section 4.8 of the [datasheet](/ref/bma456.pdf) for more information on the auxiliary interface.

The sensor communicates over I<sup>2</sup>C and SPI with two interrupt pins configurable to trigger on any of the sensor's embedded intelligence detection events. It accepts a supply voltage of 1.62 to 3.6V and consumes an average of 150&micro;A in performance mode, 14&micro;A in low power mode and just 3.5&micro;A in suspend mode. For a complete overview of the BMA456, take a look at the [datasheet](/ref/bma456.pdf)

## Connections

### Qwiic Connectors

This breakout configures the BMA456 to communicate over I<sup>2</sup>C by default and includes a pair of Qwiic connectors tied to the BMA456's power (3.3V and GND) and I<sup>2</sup>C pins (SDA/SCL) for solderless integration into a Qwiic circuit.

### Plated Through-Holes

The board also includes two 0.1"-spaced headers on either side of the board. The bottom header routes out power and ground as well as all communication pins for both I<sup>2</sup>C and SPI. 

The top header breaks out the BMA456's interrupt pins (INT1 and INT2) as well as the BMA456's auxiliary interface pins (ASDA and ASCL).

## LED

The sole LED on the board is a red power status LED to indicate when the board has power.

## Solder Jumpers

This Qwiic breakout has three solder jumpers labeled <b>LED</b>, <b>ADDR</b> and <b>I</sup>2</sup>C</b>. The list below outlines their functionality, default states and any notes on their uses.

* **LED** - The LED jumper completes the power LED circuit and is CLOSED by default. Open this jumper to disable the power LED.
* **ADDR** - The ADDR jumper sets the I<sup>2</sup>C address or enables SPI by controlling the state of the SDO pin. This three-way jumper pulls the SDO LOW by default and sets the I<sup>2</sup>C address to **0x18**. Switch the jumper to the 3.3V side to change the address to **0x19**. Open the jumper completely to free up the SDO pin for SPI communication.
* **I<sup>2</sup>C** - The **I<sup>2</sup>C** jumper pulls the BMA456's SDX and SCX pins to 3.3V through a pair of **4.7k&ohm;** resistors. This jumper is CLOSED by default. Open the jumpers to disable pull-ups on these pins.

## Board Dimensions

This board is a standard Qwiic breakout and measures 1" x 1" (25.4mm x 25.4mm) with four mounting holes that fit a 4-40 screw.