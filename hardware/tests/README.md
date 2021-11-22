# LNK302 buck converter

LinkSwitch-TN series DC/DC converter ICs combine a on/off controller and an integrated switch. LNK302 is used in a buck topology with direct feedback [(datasheet)](https://ac-dc.power.com/sites/default/files/product-docs/an37.pdf).\
[LNK302 buck converter simulation](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/Pspice/README.md#LNK302-buck-converter)

## Test setup

![Schematic](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/Pspice/Schematic.PNG)

For safety, V1 is replaced by a 60V DC source. \
Diode D1 and capacitor C3 are bypassed, since the input already is a DC source.

## Test results

![Output](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/lnk302_dc_coupling.png)&emsp;&emsp;![Output ripple](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/lnk302_ripple.png)

The left plot shows the output voltage of the buck converter.\
In the right plot the ripple on the output voltage is shown in more detail.


# LT1934-1 buck converter

LT1934-1 is a step-down DC/DC converter IC with an integrated switch, able to supply up to 60mA of output current. [(datasheet)](https://www.analog.com/media/en/technical-documentation/data-sheets/1934fe.pdf)\
[LT1934-1 buck converter simulation](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/LTspice/README.md)

## Test setup

<img src="https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/LTspice/lt1934_schematic.PNG" width=400>

Between the 3.3V output and GND, a 200 Ohm resistor is added as a load. 

## Test results

![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/lt1934_dc_coupling.png)&emsp;&emsp;![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/lt1934_ripple.png)

The left plot shows the output voltage of the buck converter.\
In the right plot the ripple on the output voltage is shown in more detail.

# Zero Cross Detection

The zero cross detector is a circuit that creates a square wave which toggles every half AC line cycle. The circuit consists of a voltage divider and a rail-to-rail opamp.\
[Zero cross detector simulation](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/Pspice/README.md#Zero-Cross-Detection)

## Test setup

<img src="https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/LTspice/zcd_schematic.PNG" width=400>

For safety, the AC source is changed to a 12V sine from the waveform generator. \
Since the input voltage has changed, resistors R5 - R7 of the resistor divider need different values. R5 had changed to 33k, R6 and R7 get a value of 100k. This way the voltage over R5 will be roughly 3V.\
U3 is replaced by OPA705, a generic rail-to-rail opamp in a more convenient dip package. [(datasheet)](https://www.ti.com/lit/ds/symlink/opa705.pdf?HQS=dis-mous-null-mousermode-dsf-pf-null-wwe&ts=1637587237061&ref_url=https%253A%252F%252Fnl.mouser.com%252F)
The power supply for the opamp (3.3V DC) will be supplied by a bench power supply.

## Test results

![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/zcd_input_output.png)\

The red trace shows the input signal for the opamp.\
The blue trace shows the square wave output signal of the opamp.

![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/tests/zcd_output.png)\

This plot shows a measurement of the output of the opamp.
