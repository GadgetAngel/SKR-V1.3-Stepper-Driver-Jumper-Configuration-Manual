# SKR-V1.3-Stepper-Driver-Jumper-Configuration-Manual
:exclamation: This project provides documentation on how to configure stepper motor driver boards and
how to use them with the SKR V1.3 3D printer controller board :exclamation:
```
 I use Git for Windows with VScode to manage this repository.  I also use Git LFS extension for .pdf and .png files.

 Install Git with LFS extension: https://git-lfs.github.com/

To Download the whole repository do the following: select the "Clone or download button" and click on "paste to clipboard" button so you can place the URL for the GitHub repository to the clipboard. Now Open Git Bash.
Change the current working directory to the location where you want the cloned directory.
Type git clone, and then paste the URL you copied earlier.
$ git clone https://github.com/GadgetAngel/SKR-V1.3-Stepper-Driver-Jumper-Configuration-Manual.git
Press Enter to create your local clone.
Now open Window explorer to the location of local clone.
```
You can download the .zip file (for this repository) from my google drive located here:

## The Whole Repository in .zip file is located on Google Drive at: https://drive.google.com/file/d/1Gv3_97y-F5aOKBmhfHuSJIC9z3NbTN3u/view?usp=sharing

## Table of Contents:

```
Stepper Driver Configurations for SKR V1.3 Board
By       @GadgetAngel

Preface......................................................................................................1
  What is a stepper motor?...................................................................................2
  Stall Detection and Sensor-less Homing.....................................................................3
    Requirements Needed to Make Sensor-less Homing Work......................................................3
POLOLU A4988.................................................................................................4
  Driver Chip Chart for POLOLU A4988.........................................................................4
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers......................................5
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers.....................8
  The (latest release of) Marlin Setup for POLOLU A4988 Drivers.............................................13
BIQU A4988..................................................................................................16
  Driver Chip Chart for BIQU 4988...........................................................................16
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................17
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................20
  The (latest release of) Marlin Setup for BIQU A4988 Drivers...............................................25
DRV8825.....................................................................................................28
  Driver Chip Chart for POLOLU DRV8825......................................................................28
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................29
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................32
  The (latest release of) Marlin Setup for DRV8825 Drivers..................................................38
BIQU LV8729.................................................................................................42
  Driver Chip Chart for BIQU LV8729.........................................................................42
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................43
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................46
  The (latest release of) Marlin Setup for BIQU LV8729 Drivers..............................................52
FYSETC LV8729...............................................................................................57
  Driver Chip Chart for FYSETC LV8729.......................................................................57
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................58
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................61
  The (latest release of) Marlin Setup for FYSETC LV8729 Drivers............................................67
LERDGE LV8729...............................................................................................72
  Driver Chip Chart for LERDGE LV8729.......................................................................72
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................73
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................76
  The (latest release of) Marlin Setup for LERDGE LV8729 Drivers............................................82
MKS LV8729..................................................................................................87
  Driver Chip Chart for MKS LV8729..........................................................................87
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers.....................................88
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers....................91
  The (latest release of) Marlin Setup for MKS LV8729 Drivers...............................................97
FYSETC S6128 V1.1..........................................................................................102
  Driver Chip Chart for FYSETC S6128.......................................................................102
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................103
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................106
  The (latest release of) Marlin Setup for FYSETC S6128 V1.1 Drivers.......................................112
FYSETC ST820...............................................................................................117
  Driver Chip Chart for FYSETC ST820.......................................................................117
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................118
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................121
  The (latest release of) Marlin Setup for FYSETC ST820 Drivers............................................127
BIQU ST820.................................................................................................133
  Driver Chip Chart for BIQU ST820.........................................................................133
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................134
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................137
  The (latest release of) Marlin Setup for BIQU ST820 Drivers..............................................143
POLOLU ST820 (STSPIN820)...................................................................................149
  Driver Chip Chart for POLOLU ST820.......................................................................149
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................150
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................153
  The (latest release of) Marlin Setup for POLOLU ST820 (STSPIN820) Drivers................................159
POLOLU MP6500..............................................................................................165
  Driver Chip Chart for POLOLU MP6500......................................................................165
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................166
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................169
  The (latest release of) Marlin Setup for POLOLU MP6500 Drivers...........................................173
POLOLU TB67S249FTG.........................................................................................178
  Driver Chip Chart for POLOLU TB67S249FTG.................................................................178
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................179
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................182
  The (latest release of) Marlin Setup for POLOLU TB67S249FTG Drivers......................................188
BIQU S109..................................................................................................193
  Driver Chip Chart for BIQU S109..........................................................................193
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................194
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................197
  The (latest release of) Marlin Setup for BIQU S109 Drivers...............................................203
FYSETC S109................................................................................................208
  Driver Chip Chart for FYSETC S109........................................................................208
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................209
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................212
  The (latest release of) Marlin Setup for FYSETC S109 Drivers.............................................218
BIQU TMC2100 Stand-alone Mode..............................................................................223
  Driver Chip Chart for BIQU TMC2100 in Stand-alone Mode...................................................223
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................224
    How to Create aa SKR V1.3 DuPont Jumper Cable to Use with Tri State Drivers............................226
  SKR V1.3 LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers......................229
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................231
  The (latest release of) Marlin Setup for BIQU TMC2100 Drivers in Stand-alone Mode........................239
MKS TMC2100 Stand-alone Mode...............................................................................244
  Driver Chip Chart for MKS TMC2100 in Stand-alone Mode....................................................244
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................245
    How to Create a SKR V1.3 DuPont Jumper Cable to Use with Tri State Drivers.............................247
  SKR V1.3 LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers......................250
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................252
  The (latest release of) Marlin Setup for MKS TMC2100 Drivers in Stand-alone Mode.........................260
BIQU TMC2130 Stand-alone Mode..............................................................................265
  Driver Chip Chart for BIQU TMC2130 in Stand-alone Mode...................................................265
  SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.......................................266
    How to Create a SKR V1.3 DuPont Jumper Cable to Use with Tri State Drivers.............................268
  SKR V1.3 LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers......................271
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................273
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in Stand-alone Mode........................281
BIQU TMC2130 SPI Mode......................................................................................286
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode....................291
  Information on Sensor-less Homing........................................................................294
  Examples of Different SPI Configurations.................................................................299
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in SPI Mode................................301
BIQU TMC2208 V3.0 Stand-alone Mode.........................................................................314
  Driver Chip Chart for BIQU TMC2208 in Stand-alone Mode...................................................314
  SKR V1.3 LEGEND of Driver Chip for Binary State Stepper Drivers..........................................315
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................318
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in Stand-alone Mode...................322
BIQU TMC2208 V3.0 One Time Programming (OTP) Mode..........................................................327
  Driver Chip Chart for BIQU TMC2208 in OTP Mode...........................................................327
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................328
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................331
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in One Time Programming (OTP) Mode....335
BIQU TMC2208 V3.0 UART Mode................................................................................340
  Driver Chip Chart for BIQU TMC2208 in UART Mode..........................................................340
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode...................344
  Examples of Different UART Configurations................................................................348
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in UART Mode..........................349
FYSETC TMC2208 V1.2 Stand-alone Mode.......................................................................359
  Driver Chip Chart for FYSETC TMC2208 in Stand-alone Mode.................................................359
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................360
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................363
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in Stand-alone Mode.................367
FYSETC TMC2208 V1.2 One Time Programming (OTP) Mode........................................................372
  Driver Chip Chart for FYSETC TMC2208 in OTP Mode.........................................................372
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................373
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................376
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in One Time Programming (OTP) Mode..380
FYSETC TMC2208 V1.2 UART Mode..............................................................................385
  Driver Chip Chart for FYSETC TMC2208 in UART Mode........................................................385
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode...................389
  Examples of Different UART Configurations................................................................393
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in UART Mode........................394
BIQU TMC2225 V1.0 Stand-alone Mode.........................................................................404
  Driver Chip Chart for BIQU TMC2225 in Stand-alone Mode...................................................404
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................405
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................408
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in Stand-alone Mode...................412
BIQU TMC2225 V1.0 One Time Programming (OTP) Mode..........................................................417
  Driver Chip Chart for BIQU TMC2225 in OTP Mode...........................................................417
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................418
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................421
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in One Time Programming (OTP) Mode....425
BIQU TMC2225 V1.0 UART Mode................................................................................430
  Driver Chip Chart for BIQU TMC2225 in UART Mode..........................................................430
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode...................434
  Examples of Different UART Configurations................................................................438
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in UART Mode..........................439
BIQU TMC2209 V1.2 Stand-alone Mode for StealthChop.........................................................449
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (StealthChop).....................................449
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................450
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................453
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for StealthChop...457
BIQU TMC2209 V1.2 Stand-alone Mode for SpreadCycle.........................................................462
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (SpreadCycle).....................................462
  SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers....................................463
  SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers...................466
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for SpreadCycle...470
BIQU TMC2209 V1.2 UART Mode................................................................................475
  Driver Chip Chart for BIQU TMC2209 in UART Mode..........................................................475
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode...................480
  Information on Sensor-less Homing........................................................................482
  Examples of Different UART Configuratins.................................................................487
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in UART Mode..........................489
BIQU TMC5160 V1.2 SPI Mode.................................................................................502
  Driver Chip Chart for BIQU TMC5160 in SPI Mode...........................................................502
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode....................507
  Information on Sensor-less Homing........................................................................510
  Examples of Different SPI Configurations.................................................................515
  The (latest release of) Marlin Setup for BIQU TMC5160 V1.2 Drivers in SPI Mode...........................517
BIQU TMC5161 V1.0 SPI Mode.................................................................................530
  Driver Chip Chart for BIQU TMC5161 in SPI Mode...........................................................530
  SKR V1.3 LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode....................535
  Information on Sensor-less Homing........................................................................538
  Examples of Different SPI Configurations.................................................................543
  The (latest release of) Marlin Setup for BIQU TMC5161 V1.0 Drivers in SPI Mode...........................545
APPENDIX A.................................................................................................558
  How to adjust the Vref on a Stepper Motor Driver board using the Potentiometer...........................558
APPENDIX B.................................................................................................560
  For the TMC drivers what's the difference between stand-alone mode and ("UART" or "SPI ") modes?.........560
  How to Calculate Vref for Non-TMC Stepper Motor Divers...................................................560
  How to Calculate Vref for TMC Stepper Motor Drivers......................................................561
  Driving Current Calculation Formulas for TMC Stepper Motor Drivers.......................................562
    #1 TMC2100 with Rs = 0.110Ω (110mΩ)....................................................................562
    #2 TMC2130 with Rs = 0.110Ω (110mΩ)....................................................................562
    #3 TMC2208 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................562
    #4 TMC2208 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................563
    #5 TMC2209 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................563
    #6 TMC2209 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................564
    #7 TMC2225 with Rs = 0.150Ω (150mΩ) for UART Mode......................................................564
    #8 TMC5160 with Rs = 0.075Ω (75mΩ) for SPI Mode........................................................564
    #9 TMC5161 with Rs = 0.062Ω (62mΩ) for SPI Mode........................................................565
    #10 TMC2225 with Rs = 0.150Ω (150mΩ) for Stand-alone Mode..............................................565
APPENDIX C.................................................................................................566
  The (Latest Release of) Marlin Setup That Is Common to ALL Stepper Motor Drivers.........................566
    Link to BIGTREETECH SKR V1.3 Instruction Manual.pdf....................................................566
    Link to BIGTREETECH SKR V1.3 Guide.pdf.................................................................566
    Link to Download Marlin 2.0.x Firmware Website.........................................................566
    Link to Pronterface Software...........................................................................567
    Link to How to Calibrate your 3D Printer...............................................................567
  SKR V1.3 Color PIN Diagram...............................................................................579
  SKR V1.3 Color Wiring Diagram............................................................................580
  SKR V1.3 Color PIN 1 Diagram.............................................................................583
  SKR V1.3 Color Schematic Diagram.........................................................................584
  SKR V1.3 Uncolored Schematic Diagram.....................................................................585
APPENDIX D.................................................................................................586
  Legends for SKR V1.3 Stepper Driver Socket Representations...............................................586
    SKR V1.3 LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers.................587
    SKR V1.3 LEGEND of Driver Chip Chart for Binary State Stepper Drivers..................................590
    SKR V1.3 LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers....................591
    SKR V1.3 LEGEND of Driver Chip Chart for Tri State Stepper Drivers.....................................593
      How to Create a SKR V1.3 DuPont Jumper Cable to Use with Tri State Drivers...........................595
    SKR V1.3 LEGEND of Driver Socket Representation for SPI Capable Stepper Motor Drivers..................596
    SKR V1.3 LEGEND of Driver Socket Representation for UART Capable Stepper Motor Drivers.................599
    SKR V1.3 LEGEND of Driver Socket Representation for Sensor-less Homing Capable Stepper Motor Drivers...602
  Examples for Stepper Driver Socket Representations.......................................................606
    Example 1 (LV8729 Driver Board; Binary State Driver) for SKR V1.3 Driver Socket Representation.........606
    Example 2 (A4988 Driver Board; Binary State Driver) for SKR V1.3 Driver Socket Representation..........607
    Example 3 (TMC2130 Driver in Stand-alone Mode; Tri State Driver) for SKR V1.3 Driver Socket 
        Representation.....................................................................................608
    Example 4 (TMC2209 UART with Sensor-less Homing) for SKR V1.3 Driver Socket Representation.............609
    Example 5 (TMC2209 UART WITHOUT Sensor-less Homing) for SKR V1.3 Driver Socket Representation..........610
    Example 6 (TMC2130 SPI with Sensor-less Homing) for SKR V1.3 Driver Socket Representation..............611
    Example 7 (TMC2130 SPI WITHOUT Sensor-less Homing) for SKR V1.3 Driver Socket Representation...........612
APPENDIX E.................................................................................................613
  Location Of “firmware.bin” File from the Marlin Compilation for SKR V1.3 Board...........................613
APPENDIX F.................................................................................................616
  Links to Reference Material..............................................................................616
    Marlin Firmware Documentation..........................................................................616
    Information on Stepper Motor Drivers and Micro-stepping................................................616
    POLOLU A4988 and BIQU A4988............................................................................617
    DRV8825................................................................................................617
    BIQU LV8729, FYSETC LV8729, LERDGE LV8729, and MKS LV8729..............................................618
    BIQU LV8729............................................................................................618
    FYSETC LV8729..........................................................................................619
    LERDGE LV8729..........................................................................................619
    MKS LV8729.............................................................................................620
    FYSETC S6128 V1.1......................................................................................620
    FYSETC ST820...........................................................................................621
    BIQU ST820.............................................................................................621
    POLOLU ST820 (STSPIN820)...............................................................................622
    POLOLU MP6500..........................................................................................622
    POLOLU TB67S249FTG.....................................................................................623
    BIQU S109 and FYSETC S109..............................................................................623
    BIQU S109..............................................................................................624
    FYSETC S109............................................................................................624
    Marlin Firmware Documentation Specific to TMC Drivers..................................................625
    Information Common to All TMC Drivers..................................................................625
    BIQU TMC2100 and MKS TMC2100...........................................................................626
    BIQU TMC2130...........................................................................................627
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2........................................627
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2 (Continued)............................628
    BIQU TMC2208 V3.0......................................................................................628
    FYSETC TMC2208 V1.2....................................................................................628
    Information Common to TMC2208 and BIQU TMC2225.........................................................629
    BIQU TMC2225 V1.0......................................................................................629
    BIQU TMC2209 V1.2......................................................................................630
    BIQU TMC5160 V1.2......................................................................................630
    BIQU TMC5161 V1.0......................................................................................631
    SKR V1.3 Board.........................................................................................631
    Facebook Groups........................................................................................632
    Miscellaneous Information..............................................................................633
APPENDIX G.................................................................................................634
  BIGTREETECH Reference Material...........................................................................634
    Original PIN Diagram...................................................................................634
    Original Wiring Diagram 1..............................................................................635
    Original Wiring Diagram 2 for STEP/DIR Mode............................................................636
    Original Wiring Diagram 3 for UART Mode................................................................637
    Original Wiring Diagram 4 for SPI Mode.................................................................638
    Original PIN 1 Diagram.................................................................................639
    Additional Original Reference Material for PIN 1 Diagram...............................................640
    Original Schematic Diagram.............................................................................641
APPENDIX H.................................................................................................642
  Filament Runout Sensor Wired to Limit Switch {X-, Y-, Z-, X+, Y+, or Z+}.................................642
    Marlin 2.0.x Setup for Filament Runout Sensor Connected to X+ Endstop Connector........................643
    Marlin 2.0.x Setup for Filament Runout Sensor..........................................................644
APPENDIX I.................................................................................................649
  Connecting SKR V1.3 to Raspberry Pi to Eliminate USB Cable...............................................649
    Wiring Diagram for Connecting SKR V1.3 to Raspberry Pi to Eliminate USB Cable..........................652
  Marlin 2.0.x Setup for Communicating with Raspberry Pi via Serial Connection on SKR V1.3 Board...........655
APPENDIX J.................................................................................................657
  Connecting SKR V1.3 with BLTouch.........................................................................657
    Wiring Diagram for Connecting SKR V1.3 with BLTouch....................................................660
  Marlin 2.0.x Firmware Setup for Connecting a BLTouch to the SKR V1.3 Board...............................661
    Understanding Marlin Firmware’s NOZZLE_TO_PROBE_OFFSET Setting.........................................665
APPENDIX K.................................................................................................680
  Connecting SKR V1.3 with PT100 Amplifier Board and PT100 Sensor..........................................680
    Instructions on How to Perform the SKR V1.3 Hardware Hack to Obtain an ADC Input on a Thermistor Port..685
  Instructions for Suppling Power to the PT100 Amplifier Board.............................................688
    Method #1 for Powering the PT100 Amplifier Board (Digital PWR).........................................689
    Method #2 for Powering the PT100 Amplifier Board (Analog PWR)..........................................690
  Technique #1 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up You PT100 to the TFT Header......691
  Technique #2 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your PT100 to the TH0 Connector..692
  Technique #2 & Method #2 (Analog PWR) Wiring Diagram for Connecting Up Your PT100 to the TH0 Connector...693
  Marlin 2.0.x Firmware Setup for Connecting a PT100 Sensor to the SKR V1.3 Board..........................695
    Marlin 2.0.x Firmware Setup via Technique #1...........................................................695
    Marlin 2.0.x Firmware Setup via Technique #2...........................................................700
APPENDIX L.................................................................................................705
  Connecting SKR V1.3 with K-Type Thermocouple Sensor and Adafruit’s AD8495 Amplifier Board................705
    Instructions on How to Perform the SKR V1.3 Hardware Hack to Obtain an ADC Input on a Thermistor Port..710
  Instructions for Suppling Power to the AD8495 Amplifier Board............................................713
    Method #1 for Powering the AD8495 Amplifier Board (Digital PWR)........................................714
    Method #2 for Powering AD8495 Amplifier Board (Analog PWR).............................................715
  Technique #1 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your K-Type Thermocouple to 
      the TFT..............................................................................................716
  Technique #2 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your K-Type Thermocouple to 
      the TH0 Connector....................................................................................717
  Technique #2 & Method #2 (Analog PWR) Wiring Diagram for Connecting Up Your K-Type Thermocouple to 
      the TH0 Connector....................................................................................718
  Marline 2.0.x Firmware Setup for Connecting a K-Type Thermocouple Sensor and Adafruit’s AD8495 
      Amplifier Board......................................................................................719
    Marlin 2.0.x Firmware Setup via Technique #1...........................................................720
    Marlin 2.0.x Firmware Setup via Technique #2...........................................................726
```
