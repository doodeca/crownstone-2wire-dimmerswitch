# LT1934-1 buck converter

LT1934-1 is a step-down DC/DC converter IC with an integrated switch, able to supply up to 60mA of output current. [datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/1934fe.pdf).


## Simulation specific components description 

The purpose of R4 and R5 is to be able to measure the current from the source and the current going into the switching regulator.\
V1 simulates a 15V DC source with a 0.15V sine ripple at 62kHz. B1 simulates a 15V DC source with noise +-0.5V.\
R3 simulates the load.

## Simulation results

![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/LTspice/15-3v3-buck-plot.PNG)

The top plot shows the input signal (V_in).\
The second plot shows output voltage V_out (green) and the current through the load resistor R3 (blue).\
The last plot shows input current of the converter IC (magenta) and the current draw from from the source (blue).


# Zero Cross Detection

This schematic simulates an opamp used for detecting a zero crossing in an AC signal. The opamp used is MCP6L01, a basic rail-to-rail opamp [datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/MCP6L01-1R-1U-2-4-1-MHz-85-uA-Op-Amps-DS20002140D.pdf). Since there's no spice model available for this opamp, the values from the datasheet were entered in the universal opamp model. 

## Simulation specific components description

V1 and V2 simulate 230V RMS voltage sources (325V pk).
B1 adds white noise to V1. 
U1 is an universal opamp (level 2) model, U2 is identical to U1. 
|Parameter|Value|
|---|---|
|Open loop voltage gain|100 k (100dB)|
|Gain bandwidth|1 MHz|
|Slew Rate|0.6V/us (=600kV/s)|
|Current Limit|20 mA|
|rail=0|rail-to-rail opamp|
|V offset|0.001|
|Input Impedance|500 M|
|Output Impedance|1 k|

## Simulation results

![Plot](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/LTspice/zcd-opamp-plot.PNG)

The top plot shows an ideal situation where the input is a perfect sine wave.\
The bottom plot introduces noise in the input (blue), which results in a bouncing of the output signal (red).
