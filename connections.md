Pins connections
================

Description of the connections among pins of the MCU, the radio module and the external parts.

Atmega-radio connections
------------------------

    ATMEGA      -> NRF24L01

    PIN 4  PD2  -> PIN 8 NRF24 (IRQ)
    PIN 15 PB1  -> PIN 3 NRF24 (CE)
    PIN 16 PB2  -> PIN 4 NRF24 (CSN)
    PIN 17 PB3  -> PIN 6 NRF24 (MOSI)
    PIN 18 PB4  -> PIN 7 NRF24 (MISO)
    PIN 19 PB5  -> PIN 5 NRF24 (SCK)

Power connections
-----------------

    ATMEGA      -> Power

    PIN 7 VCC   -> 3V
    PIN 8 GND   -> GND
    PIN 20 AVCC -> 3V (!!!)


    NRF24L01    -> Power

    PIN 1 GND   -> GND
    PIN 2 VCC   -> 3V


Programmer connections
----------------------
In order to be able to program the ATMega from the pC, you need a USB to serial converter. Important: it must allow 3V or you will burn the nrf24 module. There are several on the Market, I have used one based on the FTDI chip which allows 5V and 3.3V, see this [example](http://www.miniinthebox.com/es/programa-ftdi-basico-downloader-usb-a-ttl-ft232-para-arduino_p903425.html?currency=EUR&litb_from=paid_adwords_shopping&gclid=COje3dfj1rwCFSEHwwoddUoAIg). 

For the connections, you will need some extra components, as the DTR pin from these serial converters are not compatible with the reset pin as it is used in Arduino. An example is available at [this link](http://www.modsbyus.com/use-the-ftdi-basic-breakout-board-to-program-an-atmega328p-pu-with-optiboot/) or [this](http://www.psyelmer9.info/3/post/2012/05/may-17th-2012.html).

    ATMEGA      -> Programmer

    PIN 2 PD0   -> TX
    PIN 3 PD1   -> RX
	
	Other:
	
	GND on Programmer -> common GND on pIoT board
	VCC on Programmer -> common Vcc on pIoT board
	
	PIN 1 PC6   -> 22pF cap
	22pF cap    -> DTR
	PIN 1 PC6   -> 10Ko res
	10Ko res    -> VCC on Programmer
	
	
plus, I would also recommend a 10uF between Vcc and GND


