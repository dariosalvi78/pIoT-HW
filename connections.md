Pins connections:

ATMEGA      -> NRF24L01

PIN 4  PD2  -> PIN 8 NRF24 (IRQ)
PIN 15 PB1  -> PIN 3 NRF24 (CE)
PIN 16 PB2  -> PIN 4 NRF24 (CSN)
PIN 17 PB3  -> PIN 6 NRF24 (MOSI)
PIN 18 PB4  -> PIN 7 NRF24 (MISO)
PIN 19 PB5  -> PIN 5 NRF24 (SCK)


ATMEGA      -> Power

PIN 7 VCC   -> 3V
PIN 8 GND   -> GND
PIN 20 AVCC -> 3V (!!!)


NRF24L01    -> Power

PIN 1 GND   -> GND
PIN 2 VCC   -> 3V



ATMEGA      -> Programmer

PIN 1 PC6   -> Reset
PIN 2 PD0   -> TX
PIN 3 PD1   -> RX



you need a USB to serial converter. There are several on the Market, I have user one based on the FTDI chip which allows 5V and 3.3V (example: http://www.miniinthebox.com/es/programa-ftdi-basico-downloader-usb-a-ttl-ft232-para-arduino_p903425.html?currency=EUR&litb_from=paid_adwords_shopping&gclid=COje3dfj1rwCFSEHwwoddUoAIg). Important: it must use 3V or you will burn the nrf24 module.

Connection:

follow this link http://www.modsbyus.com/use-the-ftdi-basic-breakout-board-to-program-an-atmega328p-pu-with-optiboot/ or this: http://www.psyelmer9.info/3/post/2012/05/may-17th-2012.html
you need to connect:

GND -> GND on the pIoT node
Vcc -> Vcc on the pIoT board 
TX -> RX on the pIoT board
Rx -> Tx on the pIoT board
DTR -> a 22 pF capacitor
22pF capacitor -> Reset on the pIoT board

plus, you need a 10KO resistor between the Reset pin and the Vcc
and I would also recommend a 10uF between Vcc and GND


Use the Arduino environment:

Board: Arduino Pro or Pro mini
Processor: Atmega 328 (3.3V, 8Mhz)

