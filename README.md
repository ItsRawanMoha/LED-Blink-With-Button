# LED Blink With Button Task

Welcome to the LED Blink With Button Task! This task demonstrates how to control an LED using a button and a microcontroller. By pressing the button, you can toggle the LED on and off. 

## Introduction

The LED Blink With Button project aims to provide a practical example of interfacing a button with a microcontroller to control an LED. 

## How it Works

The project works by utilizing a pushbutton as an input device to control the state of an LED. When the pushbutton is pressed, it changes the state of the LED from on to off or vice versa. The Arduino continuously monitors the state of the pushbutton and updates the LED accordingly.

## Getting Started

### Components Required

To build this project, you will need the following components:

- Arduino board (e.g., Arduino Uno)
- LED (any color)
- Pushbutton
- Breadboard
- Jumper wires

### Steps

Follow these steps to set up the circuit:

1. Connect one leg of the pushbutton to digital pin 8 on the Arduino.
2. Connect the other leg of the pushbutton to the ground (GND) pin on the Arduino.
3. Connect the anode (longer leg) of the LED to digital pin 13 on the Arduino.
4. Connect the cathode (shorter leg) of the LED to the ground (GND) pin on the Arduino.
5. Ensure all components are securely connected to the breadboard.

| Arduino       | Pushbutton     |
| ------------- | -------------- |
| 8             | 8              |
| GND           | GND            |

| Arduino       | LED            |
| ------------- | -------------- |
| 13            | Anode          |
| GND           | Cathode        |


## Connection

A visual representation of the circuit connection is provided in the circuit design below:

![screen-gif](https://github.com/ItsRawanMoha/LED-Blink-With-Button/blob/main/Circuit-Design-LED-with-Button.png)

## Output

Once the circuit is set up and the code is uploaded to the Arduino board, you can press the pushbutton to toggle the LED on and off.

## Code
```
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 8;  // the number of the pushbutton pin
const int ledPin = 13;    // the number of the LED pin

// variables will change:
int buttonState = 0;  // variable for reading the pushbutton status

void setup() {
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT_PULLUP);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);

  // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(ledPin, HIGH);
  } else {
    // turn LED off:
    digitalWrite(ledPin, LOW);
  }
}
```
## Pictures
<img src="https://github.com/ItsRawanMoha/LED-Blink/blob/main/LED-BlinkP.jpeg" alt="Alt text" width="400" height="400">  ![screen-gif](https://github.com/ItsRawanMoha/LED-Blink-With-Button/blob/main/LED-Blink-With-ButtonG.gif)

## Conclusion

The LED Blink With Button project provides a practical demonstration of how to interface a button with a microcontroller to control an LED. 
