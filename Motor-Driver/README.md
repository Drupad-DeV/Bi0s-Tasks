# Control motor driver using Arduino UNO.
## What is Arduino UNO?
<img src ="https://user-images.githubusercontent.com/100958162/168890151-7cce3785-7166-4b5d-afaf-799c8aa38b9b.png" width = 500 height = 300 />

- Arduino UNO is a microcontroller board based on the ATmega328P. 
- It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz ceramic resonator, a USB connection, a power jack, an ICSP header and a reset button. 
- It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started

## What is motor driver (L293D)?
<img src ="https://user-images.githubusercontent.com/100958162/168889712-939a1fb1-07a3-41f7-9b89-4394d479ab70.png" align = "right" />
- A motor driver is an integrated circuit chip which is usually used to control motors in autonomous robots. 
- Motor driver act as an interface between Arduino and the motors.
- L293D consist of two H-bridge. H-bridge is the simplest circuit for controlling a low current rated motor. 
- L293D has 16 pins. That can work with 2 diffrent Motors at a same time.

### Arduino Code:
```
// C++ code
//

//Motor Setup and Pins
int speed = 3;
int in1 = 7;
int in2 = 4;
void setup()
{
  pinMode(speed, OUTPUT);
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
  //initially setting  to zero
  digitalWrite(in1, LOW);
  digitalWrite(in2, LOW);
  digitalWrite(speed, LOW);
}

void loop()
{
  direction();
  delay(1000);
  speedcontrol();
  delay(1000);
}

void direction()
{
  analogWrite(speed, 255); //speed set to max
  
  digitalWrite(in1, HIGH); // direction control 
  digitalWrite(in2, LOW);
  
  delay(2000);
  
  digitalWrite(in1, LOW);
  digitalWrite(in2, HIGH);
  
  delay(2000);
  
  digitalWrite(in1, LOW); //turning off motors
  digitalWirte(in2, LOW);
}

void speedcontrol()
{
  
}
```
#### Circuit Diagram:
![image](https://user-images.githubusercontent.com/100958162/168897504-697e5e59-ec7b-4488-9f3a-1f2f04b5ca48.png)
 
<a href = "https://www.tinkercad.com/things/41rtsIpefzh"> <img src ="https://img.shields.io/badge/Thinkercad%20File-Motor%20Driver%20Control%20-brightgreen" width = 320 align = center> </a>
