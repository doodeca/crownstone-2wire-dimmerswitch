# Crownstone 2-Wire Dimmer/switch
A repository to document the design process of the Crownstone 2-wire dimmer/switch prototype.


## Schematics 
| Version | Changes | 
|---|---|
| [V1](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.pdf) | First draft |
| [V1.1](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.1.pdf) | Replace LDO with a DC/DC converter, replace LNK3302 by LNK302, add opamp for ZCD |
| [V1.2](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.2.pdf) | Change value of R5 to 82k |
| [V1.3](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.3.pdf) | Add rotary encoder |
| [V1.4](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.4.pdf) | Add dimmer circuit, change rotary encoder |


## Simulations
[230V AC - 15V DC buck converter using LinkSwitch, half rectifier](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/Pspice/README.md#LNK302-buck-converter-half-rectiefier)\
[230V AC - 15V DC buck converter using LinkSwitch, full rectifier](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/Pspice/README.md#LNK302-buck-converter-full-rectifier)\
[3.3V buck converter using LT1934](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/LTspice/README.md#LT1934-1-buck-converter)\
[Zero Cross Detection using an opamp](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/LTspice/README.md#Zero-Cross-Detection)

## Tests
[15V DC buck converter using LinkSwitch](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/tests/README.md#lnk302-buck-converter)\
[3.3V buck converter using LT1934](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/tests/README.md#lt1934-1-buck-converter)\
[Zero Cross Detection using an opamp](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/tests/README.md#zero-cross-detection)

## Documents
[Report](https://docs.google.com/viewer?url=https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/documents/report/Stageverslag_Crownstone.pdf)

