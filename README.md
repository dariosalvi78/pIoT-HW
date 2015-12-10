<img src="http://openclipart.org/people/Scout/Chick.svg" width="10%" height="10%"/> pIoT-HW
===========================================================================================

pIoT is an open source pico/personal framework for the Internet of Things (IoT).
It includes a hardware design for low-cost, low-power, Arduino compatible boards, a C++ library for programming the board and a simple server application that stores data and offers web visualization.


This repo contains the design of the hardware board.


Requirements of the board
-------------------------

1.  it has to be compatible with the Arduino environment
2.  it must include radio communication means
2.  building the basic board should cost less than 5€
3.  it has to be able to last years with standard batteries

Design decisions
----------------

*  Microcontroller: ATMega 328p, the same as Arduino Uno
*  Radio module: nrf24L01+

Details
-------

The hardware design is simply an ATMega328p connected to an nRF24L01.
You need to program the ATMega328 following the tutorial on [Arduino to Breadboard](https://www.arduino.cc/en/Tutorial/ArduinoToBreadboard).

In this repo you can find:

*  a [Fritzing](http://fritzing.org/home/) [schema of the board](https://github.com/dariosalvi78/pIoT-HW/blob/master/pIoT.fzz)
*  the [connections schema](https://github.com/dariosalvi78/pIoT-HW/blob/master/connections.md) of the board
*  the [boards.txt](https://github.com/dariosalvi78/pIoT-HW/blob/master/boards.txt) file to be added in the hardware folder in the sketch folder of your Arduino IDE, lternatively, you can use the Arduino mini pro at 3.3V which is compatible with this one
*  [images](https://github.com/dariosalvi78/pIoT-HW/tree/master/pictures) of some prototypes

