# LNK304 buck converter

LinkSwitch-TN series DC/DC converter ICs combine a on/off controller and an integrated switch. LNK304 was chosen for it's slightly higher maximum output current of 160mA at 15V [datasheet](https://ac-dc.power.com/sites/default/files/product-docs/an37.pdf).

## Simulation specific components description 

![Schematic]()

V1 simulates a 230Vrms source at 50 hertz, R3 simulates the load.

## Simulation results

![Plot_in]()

This plot shows the input signal (red) and the rectified input (blue).

![Plot_out]()

In this plot the output voltage is shown.
