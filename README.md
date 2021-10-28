# Crownstone 2-Wire Dimmer/switch
A repository to document the design process of the Crownstone 2-wire dimmer/switch prototype.


## Schematics 
| Version | Changes | 
|---|---|
| [V1](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.pdf) | First draft |
| [V1.1](https://github.com/doodeca/crownstone-2wire-dimmerswitch/raw/main/hardware/schematics/Schematic_V1.1.pdf) | Replaced LDO with a DC/DC converter, replaced LNK3302 by LNK302, added opamp for ZCD |

## Simulations
[230V AC - 15V DC buck converter using LinkSwitch](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/Pspice/README.md#LNK302-buck-converter)
[3.3V buck converter using LT1934](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/LTspice/README.md#LT1934-1-buck-converter)
[Zero Cross Detection using an opamp](https://github.com/doodeca/crownstone-2wire-dimmerswitch/blob/main/hardware/simulations/LTspice/README.md#Zero-Cross-Detection)
