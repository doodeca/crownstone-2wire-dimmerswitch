# LNK302 buck converter

LinkSwitch-TN series DC/DC converter ICs combine a on/off controller and an integrated switch. LNK302 is used in a buck topology with direct feedback [datasheet](https://ac-dc.power.com/sites/default/files/product-docs/an37.pdf).
PI Expert's [spreadsheet](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/Pspice/LinkSwitch-TN_buck_PIExpert%20.pdf) tool is used to calculate the external component values. 

## Simulation specific components description 

![Schematic](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/Pspice/schematic.PNG)

V1 simulates a 230Vrms source at 50 hertz, R3 simulates the load.

## Simulation results

![Plot_in](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/Pspice/input_plot.PNG)

This plot shows the input signal (red) and the rectified input (blue).

![Plot_out](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/simulations/Pspice/output_plot.PNG)

In this plot the output voltage is shown.
