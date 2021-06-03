# Communication with Laser and LDR 

## Introduction

NRZ Communication with lasers on and of state. When it's on, it generates laser on LDR and when LDR's data is over normal, it generates 1 value (0 otherwise). By using lasers on and of state we are communicating with other Arduino. 

![image](https://user-images.githubusercontent.com/18538179/120644645-3e005800-c480-11eb-898a-ae1327c44e67.png)


## Setup
You need: 
- Two Arduino
- Laser
- LDR
- 10k ohm resistor
First, we'll set up the laser part after that we'll be going for the LDR part.

![image](https://user-images.githubusercontent.com/18538179/120644542-20cb8980-c480-11eb-932d-17cd607fc08c.png)

# Laser part

You directly connect the laser to Arduino.

You can change the bit you send by changing values inside the bits[];

LOW = 0 HIGH = 1.

You can change the delay of changing each bit by changing delay(200) inside the loop.

The last delay(1000) waits 1 second after sending a byte.

# LDR part




BreadBoard View

We are using 9 bit this time because the first one is the control bit.

You should test your LDR with and without laser. You can use this code : 
```
int ldrStatus = analogRead(ldrPin);
Serial.println(ldrStatus);
```
After that, you need to change the control number (800 on my code) to the number between output with laser and without laser.

Laser output: 1000
Without Laser: 600
Your control number should be: 800

Inside the 2. if there's a delay(200) it means it reads a bit by 200ms.

## Output
![image](https://user-images.githubusercontent.com/18538179/120645765-781e2980-c481-11eb-93c9-fef2e6fa9ca8.png)


