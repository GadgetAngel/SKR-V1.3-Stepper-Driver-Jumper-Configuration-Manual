# SKR-V1.3-Stepper-Driver-Jumper-Configuration-Manual
:exclamation: This project provides documentation on how to configure stepper motor driver boards and
how to use them with the SKR V1.3 3D printer controller board :exclamation:
```
 I use Git for Windows with VScode to manage this repository.  I also use Git LFS extenstion for .pdf and .png files.
```
## Table of Contents:

```
Stepper Driver Configurations for SKR V1.3 Board
By       @GadgetAngel

POLOLU A4988.................................................................................................1
  Driver Chip Chart for POLOLU A4988.........................................................................1
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers......................................2
  The (latest release of) Marlin Setup for POLOLU A4988 Drivers..............................................7
BIQU A4988..................................................................................................10
  Driver Chip Chart for BIQU A4988..........................................................................10
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................11
  The (latest release of) Marlin Setup for BIQU A4988 Drivers...............................................16
DRV8825.....................................................................................................19
  Driver Chip Chart for POLOLU DRV8825......................................................................19
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................20
  The (latest release of) Marlin Setup for DRV8825 Drivers..................................................26
BIQU LV8729.................................................................................................30
  Driver Chip Chart for BIQU LV8729.........................................................................30
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................31
  The (latest release of) Marlin Setup for BIQU LV8729 Drivers..............................................37
FYSETC LV8729...............................................................................................42
  Driver Chip Chart for FYSETC LV8729.......................................................................42
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................43
  The (latest release of) Marlin Setup for FYSETC LV8729 Drivers............................................49
LERDGE LV8729...............................................................................................54
  Driver Chip Chart for LERDGE LV8729.......................................................................54
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................55
  The (latest release of) Marlin Setup for LERDGE LV8729 Drivers............................................61
MKS LV8729..................................................................................................66
  Driver Chip Chart for MKS LV8729..........................................................................66
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................67
  The (latest release of) Marlin Setup for MKS LV8729 Drivers...............................................73
FYSETC S6128 V1.1...........................................................................................78
  Driver Chip Chart for FYSETC S6128 V1.1...................................................................78
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................79
  The (latest release of) Marlin Setup for FYSETC S6128 V1.1 Drivers........................................85
FYSETC ST820................................................................................................90
  Driver Chip Chart for FYSETC ST820........................................................................90
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................91
  The (latest release of) Marlin Setup for FYSETC ST820 Drivers.............................................97
BIQU ST820.................................................................................................103
  Driver Chip Chart for BIQU ST820.........................................................................103
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................104
  The (latest release of) Marlin Setup for BIQU ST820 Drivers..............................................110
POLOLU ST820 (STSPIN820)...................................................................................116
  Driver Chip Chart for POLOLU ST820.......................................................................116
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................117
  The (latest release of) Marlin Setup for POLOLU ST820 (STSPIN820) Drivers................................123
POLOLU MP6500..............................................................................................129
  Driver Chip Chart for POLOLU MP6500......................................................................129
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................130
  The (latest release of) Marlin Setup for POLOLU MP6500 Drivers...........................................135
POLOLU TB67S249FTG.........................................................................................140
  Driver Chip Chart for POLOLU TB67S249FTG.................................................................140
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................141
  The (latest release of) Marlin Setup for POLOLU TB67S249FTG Drivers......................................147
BIQU S109..................................................................................................152
  Driver Chip Chart for BIQU S109..........................................................................152
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................153
  The (latest release of) Marlin Setup for BIQU S109 Drivers...............................................159
FYSETC S109................................................................................................164
  Driver Chip Chart for FYSETC S109........................................................................164
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................165
  The (latest release of) Marlin Setup for FYSETC S109 Drivers.............................................171
BIQU TMC2100 Stand-alone Mode..............................................................................176
  Driver Chip Chart for BIQU TMC2100 in Stand-alone Mode...................................................176
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................177
    How to Create a SKR V1.3 Dupont Jumper Cable to Use with Tri State Drivers.............................179
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................182
  The (latest release of) Marlin Setup for BIQU TMC2100 Drivers in Stand-alone Mode........................190
MKS TMC2100 Stand-alone Mode...............................................................................195
  Driver Chip Chart for MKS TMC2100 in Stand-alone Mode....................................................195
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................196
    How to Create a SKR V1.3 Dupont Jumper Cable to Use with Tri State Drivers.............................198
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................201
  The (latest release of) Marlin Setup for MKS TMC2100 Drivers in Stand-alone Mode.........................209
BIQU TMC2130 Stand-alone Mode..............................................................................214
  Driver Chip Chart for BIQU TMC2130 in Stand-alone Mode...................................................214
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................215
    How to Create a SKR V1.3 Dupont Jumper Cable to Use with Tri State Drivers.............................217
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................220
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in Stand-alone Mode........................228
BIQU TMC2130 SPI Mode......................................................................................233
  Driver Chip Chart for BIQU TMC2130 in SPI Mode...........................................................233
  Examples of Different SPI Configurations.................................................................238
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in SPI Mode................................240
BIQU TMC2208 V3.0 Stand-alone Mode.........................................................................253
  Driver Chip Chart for BIQU TMC2208 V3.0 in Stand-alone Mode..............................................253
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................254
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in Stand-alone Mode...................259
BIQU TMC2208 V3.0 One Time Programming (OTP) Mode..........................................................264
  Driver Chip Chart for BIQU TMC2208 V3.0 in OTP Mode......................................................264
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................265
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in One Time Programming (OTP) Mode....270
BIQU TMC2208 V3.0 UART Mode................................................................................275
  Driver Chip Chart for BIQU TMC2208 V3.0 in UART Mode.....................................................275
  Examples of Different UART Configurations................................................................280
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in UART Mode..........................281
FYSETC TMC2208 V1.2 Stand-alone Mode.......................................................................291
  Driver Chip Chart for FYSETC TMC2208 V1.2 in Stand-alone Mode............................................291
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................292
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in Stand-alone Mode.................297
FYSETC TMC2208 V1.2 One Time Programming (OTP) Mode........................................................302
  Driver Chip Chart for FYSETC TMC2208 V1.2 in OTP Mode....................................................302
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................303
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in One Time Programming Mode........308
FYSETC TMC2208 V1.2 UART Mode..............................................................................313
  Driver Chip Chart for FYSETC TMC2208 V1.2 in UART Mode...................................................313
  Examples of Different UART Configurations................................................................318
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in UART Mode........................319
BIQU TMC2225 V1.0 Stand-alone Mode.........................................................................329
  Driver Chip Chart for BIQU TMC2225 V1.0 in Stand-alone Mode..............................................329
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................330
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in Stand-alone Mode...................335
BIQU TMC2225 V1.0 One Time Programming (OTP) Mode..........................................................340
  Driver Chip Chart for BIQU TMC2225 V1.0 in OTP Mode......................................................340
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................341
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in One Time Programming (OTP) Mode....346
BIQU TMC2225 V1.0 UART Mode................................................................................351
  Driver Chip Chart for BIQU TMC2225 V1.0 in UART Mode.....................................................351
  Examples of Different UART Configurations................................................................356
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in UART Mode..........................357
BIQU TMC2209 V1.2 Stand-alone Mode for StealthChop.........................................................367
  Driver Chip Chart for BIQU TMC2209 V1.2 in Stand-alone Mode (StealthChop)................................367
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................368
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for StealthChop...373
BIQU TMC2209 V1.2 Stand-alone Mode for SpreadCycle.........................................................378
  Driver Chip Chart for BIQU TMC2209 V1.2 in Stand-alone Mode (SpreadCycle)................................378
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................379
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for SpreadCycle...384
BIQU TMC2209 V1.2 UART Mode................................................................................389
  Driver Chip Chart for BIQU TMC2209 V1.2 in UART Mode.....................................................389
  Examples of Different UART Configurations................................................................394
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in UART Mode..........................396
BIQU TMC5160 V1.2 SPI Mode.................................................................................409
  Driver Chip Chart for BIQU TMC5160 V1.2 in SPI Mode......................................................409
  Examples of Different SPI Configurations.................................................................414
  The (latest release of) Marlin Setup for BIQU TMC5160 V1.2 Drivers in SPI Mode...........................416
BIQU TMC5161 V1.0 SPI Mode.................................................................................429
  Driver Chip Chart for BIQU TMC5161 V1.0 in SPI Mode......................................................429
  Examples of Different SPI Configurations.................................................................434
  The (latest release of) Marlin Setup for BIQU TMC5161 V1.0 Drivers in SPI Mode...........................436
APPENDIX A.................................................................................................449
  How to adjust the Vref on a Stepper Motor Driver board using the Potentiometer...........................449
APPENDIX B.................................................................................................451
  For the TMC drivers what's the difference between stand-alone mode and ("UART" or "SPI ") modes?.........451
  How to Calculate Vref for Non-TMC Stepper Motor Divers...................................................451
  How to Calculate Vref for TMC Stepper Motor Drivers......................................................452
  Driving Current Calculation Formulas for TMC Stepper Motor Drivers.......................................453
    #1 TMC2100 with Rs = 0.110Ω (110mΩ)....................................................................453
    #2 TMC2130 with Rs = 0.110Ω (110mΩ)....................................................................453
    #3 TMC2208 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................453
    #4 TMC2208 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................454
    #5 TMC2209 with Rs = 0.110 (110m) for Stand-alone Mode..............................................454
    #6 TMC2209 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................455
    #7 TMC2225 with Rs = 0.150Ω (150mΩ) for UART Mode......................................................455
    #8 TMC5160 with Rs = 0.075Ω (75mΩ) for SPI Mode........................................................455
    #9 TMC5161 with Rs = 0.062Ω (62mΩ) for SPI Mode........................................................456
   #10 TMC2225 with Rs = 0.150 (150m) for Stand-alone Mode..............................................456
APPENDIX C.................................................................................................457
  The (Latest Release of) Marlin Setup That Is Common to ALL Stepper Motor Drivers.........................457
    Link to BIGTREETECH SKR V1.3 Instruction Manual.pdf....................................................457
    Link to BIGTREETECH SKR V1.3 Guide.pdf.................................................................457
    Link to Pronterface Software...........................................................................458
    Link to How to Calibrate your 3D Printer...............................................................458
    SKR V1.3 Color PIN Diagram.............................................................................470
    SKR V1.3 Color Wiring Diagram..........................................................................471
    SKR V1.3 Color PIN 1 Diagram...........................................................................474
    SKR V1.3 Color Schematic Diagram.......................................................................475
    SKR V1.3 Uncolored Schematic Diagram...................................................................476
APPENDIX D.................................................................................................477
  Legends for SKR V1.3 Stepper Driver Socket Representations...............................................477
    SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers.................478
    SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers..................................481
    SKR V1.3 LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers....................482
    SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.....................................484
      How to Create a SKR V1.3 DuPont Jumper Cable to Use with Tri State Drivers...........................486
    SKR V1.3 LEGEND of Driver Socket Representation for SPI Capable Stepper Motor Drivers..................487
    SKR V1.3 LEGEND of Driver Socket Representation for UART Capable Stepper Motor Drivers.................488
    SKR V1.3 LEGEND of Driver Socket Representation for Sensor-less Homing Capable Stepper Motor Drivers...489
  Examples of Driver Socket Representations................................................................490
    Example 1 (LV8729 Driver Board; Binary State Driver) for SKR V1.3 Driver Socket Representation.........490
    Example 2 (A4988 Driver Board; Binary State Driver) for SKR V1.3 Driver Socket Representation..........491
    Example 3 (TMC2130 Stand-alone Mode; Tri State Driver) for SKR V1.3 Driver Socket Representation.......492
    Example 4 (TMC2209 UART Driver Board) for SKR V1.3 Driver Socket Representation........................493
    Example 5 (TMC2130 SPI Driver Board) for SKR V1.3 Driver Socket Representation.........................494
APPENDIX E.................................................................................................495
  Location Of “firmware.bin” File from the Marlin Compilation for SKR V1.3 Board...........................495
APPENDIX F.................................................................................................498
  Links to Reference Material..............................................................................498
    Marlin Firmware Documentation..........................................................................498
    Information on Stepper Motor Drivers and Micro-stepping................................................498
    POLOLU A4988 and BIQU A4988............................................................................499
    DRV8825................................................................................................499
    BIQU LV8729, FYSETC LV8729, LERDGE LV8729, and MKS LV8729..............................................500
    BIQU LV8729............................................................................................500
    FYSETC LV8729..........................................................................................501
    LERDGE LV8729..........................................................................................501
    MKS LV8729.............................................................................................502
    FYSETC S6128 V1.1......................................................................................502
    FYSETC ST820...........................................................................................503
    BIQU ST820.............................................................................................503
    POLOLU ST820 (STSPIN820)...............................................................................504
    POLOLU MP6500..........................................................................................504
    POLOLU TB67S249FTG.....................................................................................505
    BIQU S109 and FYSETC S109..............................................................................505
    BIQU S109..............................................................................................506
    FYSETC S109............................................................................................506
    Marlin Firmware Documentation Specific to TMC Drivers..................................................507
    Information Common to All TMC Drivers..................................................................507
    BIQU TMC2100 and MKS TMC2100...........................................................................508
    BIQU TMC2130...........................................................................................509
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2........................................509
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2 (Continued)............................510
    BIQU TMC2208 V3.0......................................................................................510
    FYSETC TMC2208 V1.2....................................................................................510
    Information Common to TMC2208 and BIQU TMC2225.........................................................511
    BIQU TMC2225 V1.0......................................................................................511
    BIQU TMC2209 V1.2......................................................................................512
    BIQU TMC5160 V1.2......................................................................................512
    BIQU TMC5161 V1.0......................................................................................513
    SKR V1.3 Board.........................................................................................513
    Facebook Groups........................................................................................514
    Miscellaneous Information..............................................................................515
APPENDIX G.................................................................................................516
  BIGTREETECH Reference Material...........................................................................516
    Original PIN Diagram...................................................................................516
    Original Wiring Diagram 1..............................................................................517
    Original Wiring Diagram 2 for STEP/DIY Mode............................................................518
    Original Wiring Diagram 3 for UART Mode................................................................519
    Original Wiring diagram 4 for SPI Mode.................................................................520
    Original PIN 1 Diagram.................................................................................521
    Additional Original Reference Material for PIN 1 Diagram...............................................522
    Original Schematic Diagram.............................................................................523
```
