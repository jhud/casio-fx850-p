# Casio FX850-P programs

Programs for the CASIO FX850-P pocket computer.
Use at your own risk - I accept no responsibility for damage to yourself, others, or your hardware.


## 850TERM.bas

A terminal program to allow you to interact with the serial port, use telnet, dial BBSes, interact with remote computers, etc.
Only uppercase is supported at the moment - enough to write Hayes-style AT modem commands and interact with BBSes.

### Instructions

BS key is backspace


## 850COM.bas

A simple serial communications program to allow you to interact with the serial port in a very basic way.

Input characters, hit execute, and then receive a response from the device or loopback connecton.



# Hardware info

## Scancodes
Left arrow = 29
Right arrow = 28
Up = 30
Down = 31
Caps = 15
Shift = 14
Insert = 18
BS = 8


## Serial comms

Baud Rate code
1 = 150
2 = 300
3 = 600
4 = 1200
5 = 2400
6 = 4800


ie `SAVE “COM0:6″` saves at 4800 baud


## Hardware

The 30-pin output port has a full UART at 5V level. You need an RS-232 level shifter and inverter to use it as RS-232.


### Saving

Save to modem/serial @300 Baud, no flow control:
`SAVE "COM0:2,N,8,1,N,N,N,N,N"`


### Loading

Load from modem/serial @300 Baud, no flow control:
`LOAD "COM0:2,N,8,1,N,N,N,N,N"`
Then press BREAK when the transfer is done.


### BASIC usage example

```
15 OPEN “COM0:6,N,8,1,N,N,N,N,N” AS #1
```
