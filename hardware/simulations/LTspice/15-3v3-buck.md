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
