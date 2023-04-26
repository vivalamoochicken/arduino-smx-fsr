# StepManiaX (SMX) Gen4+ with Arduino Controlled Force Sensitive Resistors 
## Table of Contents
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Installation](#installation)
  - [Credits](#credits)

## Introduction
This guide is meant to be supplementary material to the existing guide [teejusb/fsr](https://github.com/teejusb/fsr). 
For setting up an Arduino/Teensy board to work with the SMX FSRs, please follow that guide and the ones also listed within it. The concept is the same, and I used jumper cables to bridge the connection to the stock FSRs as seen in the [Installation](#installation) section.

This implementation is meant to preserve as much of the base hardware as possible in the SMX pad to ensure it can be converted back to be played with the orignal SMX software. The only component removed from the pad is the power switch/adapter at the front of the pad where the power cable is connected so that the new wires that go to the FSRs can go into it externally as this particular implementation houses the Arduino outside of the pad. This guide will go into more detail about suggestions on better ways to house the Arduino and wires in the [Installation](#installation) section.

## Installation
Setting up FSRs for gameplay with an app to adjust the sensitivities happens in three parts.
1. [Setup the hardware.](https://github.com/teejusb/fsr) The only difference between the Arduino implemenation for normal style DDR/ITG pads and SMX pads as far as sensors go is the ability to use the existing SMX FSRs without needing to remove them from the pads like you would traditional sensors in a normal style pad. You can see an example of how jumper cables can be wired into the existing SMX FSR molex connector below:
<p align="center">
    <img src="img/smx%20fsr.jpg" height="350px" />
</p>

3. 
4. [Stand up the server.](https://github.com/vlnguyen/itg-fsr/tree/master/server) Create API endpoints for interacting with the Arduino and with a local profile database.
5. [Run the web client.](https://github.com/vlnguyen/itg-fsr/tree/master/client) Once the client is running, the web app can be accessed by any device with a browser (phone, tablet, computer) to manage user profiles and sensor thresholds for up to two pads.



## Credits
- Thank you [teejusb](https://github.com/teejusb) and [VincentITG](https://github.com/vlnguyen)! Between Vincent's easy to follow picture guide and instructions from both guides, I was able to successfully implement the Arduino FSR method with my SMX Gen 4 pad. 
- [teejusb/fsr](https://github.com/teejusb/fsr)  [vlnguyen/itg-fsr](https://github.com/vlnguyen/itg-fsr)
- Please refer to these guides for setting up Arduino/Teensy board connections for general FSR use. The concept for the SMX pad is almost exactly the same.

