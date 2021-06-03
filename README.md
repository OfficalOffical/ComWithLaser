# Communication with Laser and LDR 

## Introduction

Basic NRZ Communication with laser and LDR using two Arduino. This program uses arduino codes to do 
## Setup
You need: 
- Two Arduino
- Laser
- LDR
- 10k ohm resistor
First we'll set up laser part after that we'll going for LDR part.
# Laser part

You directly connect the laser to Arduino.

You can change bit you send by changing values inside the bits[];

LOW = 0 HIGH = 1.

You can change delay of changing each bit by changing delay(200) inside the for loop.

The last delay(1000) waits 1 second after sending a byte.

# LDR part

![BreadBoard View](https://prnt.sc/w6eij8)

BreadBoard View

We are using 9 bit this time becouse the first one is control bit.

You should test your LDR with and without laser. You can use this code : 
```
int ldrStatus = analogRead(ldrPin);
Serial.println(ldrStatus);
```
After that you need to change control number (800 on my code) to number between output with laser and without laser.

Laser output : 1000
Without Laser : 600
Your control number should be : 800

Inside the 2. if there's a delay(200) it means it reads a bit by 200ms.


## SUM 

At the end it should look like ![this](https://prnt.sc/w6eobm)

And your code should looke like ![this](https://prnt.sc/w6eokk)



