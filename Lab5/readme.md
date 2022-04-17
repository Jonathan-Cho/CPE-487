# Lab 5

[Lab 5 Instructions](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-5)


## Siren

### Project Files
Source Files (VHDL): dac_if, tone, wail, siren
Constraint File: siren

### Observations
 - The speaker plays a single wail on loop without variation.
    - This wail does not change in how loud it is.



## Modifications

### Project Files ([Provided](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-5/Modifications))
Source Files (VHDL): dac_if, tone, wail, siren
Constraint File: siren

### Observations
- The speaker now changes the speed of the period of the wail and the pitch of the wail when using the switches on the board. 
- The wail no longer has a triangular wave; it abruptly changes frequency instead of smoothly 
- When using the switches, the wail eventually reaches a single pitch of high frequency.
    - I did not figure out how to reset this outside of programming the device again.
