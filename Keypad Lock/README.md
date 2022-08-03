# Keypad Lock

![image](https://user-images.githubusercontent.com/100958162/173556740-05de2223-215e-4d94-8a82-b3232d56464d.png)

## Prototype:

- A arduiono based circuit having a 4X4 keypad that could verify the password or Pin given and simulate the Servo motor, that could have been connected to a physical door or personal vault.
- An Extra Component piezo buzzer was added to the Circuit to indicate various states of the system audibly. 
- A single beep could be heard for Lock state and double beep for Unlock state.
- Also pressing "#" would 

### Circuit In Thinkercad: 

![image](https://user-images.githubusercontent.com/100958162/182664842-1e34bb19-f558-435f-99be-c10e5e01f9be.png)

### Components Used: 

![image](https://user-images.githubusercontent.com/100958162/182665290-a5522789-9b17-4085-8d7b-35313cd742a6.png)

### Circuit Diagram :

![image](https://user-images.githubusercontent.com/100958162/182665467-533e1f5a-3fb7-4e21-95dc-57eb8074f2f4.png)

### Code: 
```
// C++ code
//

#include <Keypad.h>

#include <Servo.h>

Servo motor;

const byte ROWS = 4;
const byte COLS = 4;
char keys[ROWS][COLS] = {
{'1','2','3','A'},
{'4','5','6','B'},
{'7','8','9','C'},
{'*','0','#','D'}
};

byte rowPins[ROWS] = { 11,10,9,8 };
byte colPins[COLS] = { 7,6,5,4 };  //Assigning Arduiono pins for each buttons
int buzz = 12;
int count = 0;
char* password = "48625"; //Pin to verify

Keypad keypad = Keypad( makeKeymap(keys), rowPins, colPins, ROWS, COLS );


void setup(){
  Serial.begin(9600);
  pinMode(12, OUTPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  motor.attach(2);
  tone(12, 1661, 1000);
  delay(10);
  tone(12, 0, 1000);
  motor.write(0);
}

void loop()
{
  char key = keypad.getKey();  //Reading the button pressed on 4X4 Keypad
  if (key == '*' || key == '#')
  {
    count = 0;
    tone(12, 1661, 1500);
    delay(1000);
    tone(12, 0, 1000);
    motor.write(0);
    Serial.println(count);
  }
  if (key == password[count])   //Incresing "count" if each character is verified
  {
    count ++;
    Serial.println(count);
  }
  if (count == 5)   //Password Verified State
  {
    digitalWrite(LED_BUILTIN, HIGH);
    tone(12, 1661, 1000);  //Playing the buzzer
    delay(100);
    tone(12, 0, 1000);
    delay(100);
    tone(12, 1661, 1000);
    delay(100);
    tone(12, 0, 1000);
    motor.write(90);  //Rotating the Servo
  }
  tone(0, 523, 1000);   // play tone 60 (C5 = 523 Hz)
  noTone(0);
  delay(10);   //Delay a little bit to improve simulation performance
}
```

