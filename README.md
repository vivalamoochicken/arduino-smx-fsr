# StepManiaX (SMX) Gen4+ with Arduino Controlled Force Sensitive Resistors 
## Table of Contents
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [P](#preliminary-reads-credits)
    - [SMX and Traditional Style Pad Differences?](#why-use-fsrs)
  - [Credits](#credits)

## Introduction
This guide is meant to be supplementary material to the existing guide by [teejusb/fsr](https://github.com/teejusb/fsr) and general Arduino Leonardo implementation from [vlnguyen/itg-fsr](https://github.com/vlnguyen/itg-fsr). 

For setting up an Arduino/Teensy board to work with the SMX FSRs, please follow these guides. The concept is the same, and I used jumper cables to bridge the connection to the stock FSRs as seen below:
<p align="center">
    <img src="img/smx%20fsr.jpg" height="350px" />
</p>

This implementation is meant to preserve as much of the base hardware as possible in the SMX pad to ensure it can be switched back to be played with the orignal software. The only component removed from the pad is the power switch/adapter at the front of the pad where the power cable is connected so that the new wires that go to the FSRs can go into it externally as this particular implementation houses the Arduino outside of the pad. This guide will go into more detail about suggestions on better ways to house the Arduino and wires in the [Installation](#installation) section.

### SMX and Traditional Style Pad Differences?
- For the purposes of using an Arduino/Teensy setup in an SMX style pad, the main differences will be how the wires are routed throughout the pad(s).
- In order to get the wires to the area that houses the SMX PCB and 
  - Unlike contact sensors which are only ON or OFF, we can determine whether a panel is activated by defining a variable actuation threshold on each individual 


## Installation
Setting up FSRs for gameplay with an app to adjust the sensitivities happens in three parts.
1. [Setup the hardware.](https://github.com/vlnguyen/itg-fsr/tree/master/fsr) Connect FSRs into an Arduino and flash it with code that will handle joystick inputs.
2. [Stand up the server.](https://github.com/vlnguyen/itg-fsr/tree/master/server) Create API endpoints for interacting with the Arduino and with a local profile database.
3. [Run the web client.](https://github.com/vlnguyen/itg-fsr/tree/master/client) Once the client is running, the web app can be accessed by any device with a browser (phone, tablet, computer) to manage user profiles and sensor thresholds for up to two pads.

## Credits
- Thank you [teejusb](https://github.com/teejusb) and [VincentITG](https://github.com/vlnguyen)! Between Vincent's easy to follow picture guide and instructions from both guides, I was able to successfully implement the Arduino FSR method with my SMX Gen 4 pad. 
- [teejusb/fsr](https://github.com/teejusb/fsr)  [vlnguyen/itg-fsr](https://github.com/vlnguyen/itg-fsr)
- Please refer to these guides for setting up Arduino/Teensy board connections for general FSR use. The concept for the SMX pad is almost exactly the same.

