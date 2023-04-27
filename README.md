# AutoPark

This is the central repository for all the code written for the '22 - '23 AutoPark project. None of the code is actually part of this repo. Instead, this repo has multiple submodules, each of which contains the actual code. If someone wishes to work with the code, find the relevant submodule then clone it, rather than working in this repo. Below is a list of what each submodule contains.

## autopark

This repository contains a large chunk of the code used by the embedded portions of the project. This includes the wireless fob, the state machine used in the cart, the code to drive the screen, and the code to manage the ultrasonic sensors.

## DemandGPSParser

This repository contains the Arduino code to interface with an Arduino Ultimate GPS. It is styled such that when the current location is desired, simply call a function. No constant loop must be maintained, which makes integrating it into other code is simpler.

## EthernetAPI

This repository contains Python code to allow for sending and receiving messages over a local network. This was used for communication between a BeagleBone Black and a Jetson Nano that were directly connected using Ethernet (hence the name). One device is the server, and the other is the client. Once the initial connection is established, messages can be sent or checked for whenever the program wants. Messages are of a fixed length, and include a header which can be used to distinguish the purpose of the message.

## gps_serial

This repository contains Python code for interfacing with an Arduino Ultimate GPS over serial. It follows essentially the same format as the DemandGPSParser, except for Python instead.

## rcJetson

This repository contains some example code for issuing orders over EthernetAPI to a BeagleBone Black. It was not actually used in practice, but kept for posterity.

## rcPWM

This repository contains the code used on the BeagleBone Black for receiving orders from the Jetson while controlling the vehicle. The main branch is used for the golf cart, while the RC-Car-Semester-One branch is what was used for the first semester RC car.

## YoungWoodsCar

This repository is the actual code which ran on the Jetson for controlling the golf cart. It is a fork of the Donkeycar project, with some tweaks for using the EthernetAPI to issue orders and custom bindings for use with an Xbox controller.

## Autpark-CV

## Autport-ReverseControl
