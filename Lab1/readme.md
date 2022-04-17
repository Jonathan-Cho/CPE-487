# Lab 1 
### Process

#### Downloading Vivado
1. Downloaded Vivado by following the [instructions](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7) provided by my professor
2. The first time downloading, I had not disabled my antivirus software so Vivado did not download all the necessary files
3. Uninstalled Vivado
4. Redownloaded Vivado using the same instructions with my antivirus disabled

[Lab 1 Instructions](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-1)

## Generating Bit Stream // Ledec

#### Creating the project
1. Create a new project after launching the software
2. Create a source file named leddec and selecting VHD as the targer and source languages
3. Create a constraint file named leddec
4. Selecting the Nexys A7-100t  board as the board to be used for the project
5. Inputting [VHD Code](https://github.com/kevinwlu/dsd/blob/master/Nexys-A7/Lab-1/leddec.vhd) provided by my professor in the source file
6. Adding the [constraints](https://github.com/kevinwlu/dsd/blob/master/Nexys-A7/Lab-1/leddec.xdc) provided by my professor


#### Generating bitstream
1. Click generate bitstream
2. Connected my board and turned it on
3. Connected the board to the hardware manager
4. Downloaded the implementation to the board
5. Used the switches to follow gray's code:
    - Switch order:
      ```
      ON = t, OFF = f, SWITCH = s[n]
      Example: s5f = turn switch 5 off
      Gray's code: 0-1-3-2-6-7-5-4-C-d-F-E-A-b-9-8
                        Switch: 3 2 1 0             Bits
      s0f - 0                   f f f f     =       0 0 0 0
      s0t - 1                   f f f t     =       0 0 0 1
      s1t - 3                   f f t t     =       0 0 1 1
      s0f - 2                   f f t f     =       0 0 1 0
      s2t - 6                   f t t f     =       0 1 1 0
      s0t - 7                   f t t t     =       0 1 1 1
      s1f - 5                   f t f t     =       0 1 0 1
      s0f - 4                   f t f f     =       0 1 0 0
      s3t - C                   t t f f     =       1 1 0 0
      s0t - D                   t t f t     =       1 1 0 1
      s1t - F                   t t t t     =       1 1 1 1
      s0f - E                   t t t f     =       1 1 1 0
      s2f - A                   t f t f     =       1 0 1 0
      s0t - B                   t f t t     =       1 0 1 1
      s1f - 9                   t f f t     =       1 0 0 1
      s0f - 8                   t f f f     =       1 0 0 0
      ```


## Hex Count

