# PWM [Pulse With modulation]
## What is PWM?

-PWM stands for Pulse Width Modulation and it is a technique used in controlling the brightness of LED, speed control of DC motor, controlling a servo motor or where you have to get analog output with digital means.

### Controlling the brightness of LED usin PWM PIN:
- Thinkercard Circuit:
- A simple Circuit involving an LED that was connected to one of the PWM pin (10 here).

![image](https://user-images.githubusercontent.com/100958162/182669050-ab16bf4d-520c-48f6-8e90-064ea6426b07.png)

## Arduiono Code:
```
// C++ code
//
int i = 0;

int j = 0;

void setup()
{
  pinMode(10, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  for (i = 0; i <= 255; i += 3) {
    analogWrite(10, i);
    delay(30); // Wait for 30 millisecond(s)
    Serial.println(i);
  }
  for (j = 255; j >= 0; j -= 3) {
    analogWrite(10, j);
    delay(30); // Wait for 30 millisecond(s)
    Serial.println(j);
  }
}
```
- The Changes on the LED can be noted and also was printed on Serial Monitor 

![OUT](https://user-images.githubusercontent.com/100958162/182671039-59d8a42b-3033-4d84-99a0-cc851a5ee728.gif)

<a href = "https://www.tinkercad.com/things/4WJedpvyNyf-brightness-of-led-using-pwm/editel"> <img src ="https://img.shields.io/badge/Thinkercad%20File-Click%20Here%20to%20Simulate-brightgreen" width = 320 align = center> </a>
