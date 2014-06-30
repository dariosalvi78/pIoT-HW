pIoT-HW
=======

pIoT is an open source pico/personal framework for the Internet of Things (IoT).
It includes a hardware design for low-cost, low-power, Arduino compatible boards, a C++ library for programming the board and a simple server application that stores data and offers web visualization.


This repo contains the design of the hardware board.


Main requirements:
------------------

1.  it has to be compatible with the Arduino environment
2.  it must include radio communication means
2.  building the basic board shall cost less than 5€
3.  it has to be able to last years with standard batteries

Design decisions:
-----------------

*  Microcontroller: ATMega 328p, the same as Arduino Uno
*  Radio module: nrf24L01+

Details:
--------

In this repo yuo can find:

1.  a [Fritzing](http://fritzing.org/home/) [schema of the board](https://github.com/dariosalvi78/pIoT-HW/blob/master/pIoT.fzz)
2.  the [detailed documentation](https://github.com/dariosalvi78/pIoT-HW/wiki) about the board design
3.  images about prototypes

