Push Button Counter using Arduino
This project demonstrates how to use a push button with an Arduino Uno to implement a simple counter. Each time the button is pressed, the counter increases by one, and the count is displayed via the Serial Monitor.

# Components Used:
Arduino Uno R3
Push Button
10kΩ Resistor
Breadboard (optional)
Jumper Wires

# Circuit Description
One leg of the push button is connected to Digital Pin 2 on the Arduino.
The other leg is connected to GND through a 10kΩ pull-down resistor.
The same leg of the push button is also connected to +5V when the button is pressed.

# Code Functionality
Initializes pin 2 as an input.
Monitors the state of the button in the loop().
If a rising edge (LOW to HIGH transition) is detected, it increments the counter.
Prints the current count to the Serial Monitor.
A short debounce delay is added to avoid multiple readings from a single press.

# How It Works
The Arduino checks if the button is pressed.
If pressed (HIGH) and was previously not pressed (LOW), it increments the counter.
The updated count is printed using Serial.print().
A small delay (200ms) is used for button debouncing.
