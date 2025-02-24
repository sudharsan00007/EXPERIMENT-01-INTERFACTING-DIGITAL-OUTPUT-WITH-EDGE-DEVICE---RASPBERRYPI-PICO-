# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---RASPBERRYPI-PICO-
## NAME: SUDHARSAN S
## DEPARTMENT : CSE 
## ROLL NO :212224040335
## DATE OF EXPERIMENT : 24.02.2025

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
Computer with Thonny IDE
## THEORY
Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.

Digital Output refers to controlling external devices like LEDs, buzzers, or relays using GPIO (General Purpose Input Output) pins. A GPIO pin can be set to HIGH (3.3V) or LOW (0V) to turn the device ON or OFF.

## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)
LED BLINK
```
from machine import Pin
from utime import sleep
led1 = Pin(0,Pin.OUT)
while True:
    led1.toggle()
    sleep(1)
```
3LED'S Blink
```
from machine import Pin
from utime import sleep
led1 = Pin(0,Pin.OUT)
led2 =Pin(2,Pin.OUT)
led3 =Pin(28,Pin.OUT)

while True:
    led1.toggle()
    sleep(1)

    led2.toggle()
    sleep(1.1)
    
    led3.toggle()
    sleep(1.2)
    
   ```
LED'S WITH BUZZER
```
from machine import Pin
from utime import sleep
led1 = Pin(0,Pin.OUT)
led2 =Pin(2,Pin.OUT)
led3 =Pin(28,Pin.OUT)
buzz=Pin(3,Pin.OUT)
while True:
    led1.toggle()
    sleep(1)
    buzz.toggle()
    sleep(1)
    led2.toggle()
    sleep(1.1)
    buzz.toggle()
    sleep(1.1)
    led3.toggle()
    sleep(1.2)
    buzz.toggle()
    sleep(1.2)
```


 



 


## OUPUT
![image](https://github.com/user-attachments/assets/04ae75c6-1c41-4953-b17b-8bc61a8930dd)

![image](https://github.com/user-attachments/assets/3aad3c2d-27b2-435e-834f-f368616f5504)

![image](https://github.com/user-attachments/assets/3159007b-df7b-45c9-acc0-75770f500415)




 
## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at 1-second intervals, confirming the proper interfacing of a digital output.
