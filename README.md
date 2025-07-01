 # Arduino Multi-Button LED Control
  This Arduino project demonstrates a simple control system where three pushbuttons independently control three LEDs. Each button corresponds to a specific LED: when the button is pressed, its associated LED turns on; when the button is released, the LED turns off. This project highlights the basic principles of digital input and output using an Arduino microcontroller.
 ## Purpose and Usefulness

This project is a practical example of digital control and interfacing, which is foundational in electronics, automation, and embedded systems. It is useful for:
- Learning how to read digital inputs (buttons).
-  Understanding how to control outputs (LEDs).
-  racticing circuit design with pull-down resistors to ensure stable input readings.
-  erving as a stepping stone for more advanced applications like keypad control, relay switching, or interactive user interfaces.

This simple configuration can be adapted to:
 - Create status indicators.
 - Build basic user input panels.
 - Prototype control panels for more complex devices.

 ## Description System Works

The project uses an Arduino board to detect the state of three pushbuttons connected to digital input pins. Each button can be in one of two states:
 - Pressed (HIGH voltage).
 - Released (LOW voltage).

When the Arduino reads a HIGH signal on a button pin, it sets the corresponding LED pin HIGH, supplying voltage to turn the LED on. If the button is released, the Arduino sets the LED pin LOW, turning the LED off.

To prevent false readings when buttons are not pressed, each button has a 10k Ohm pull-down resistor. This resistor ensures the input pin reads a clean LOW signal when the button is open.

## Design and Components

Hardware Components
 - Arduino Uno (or compatible board).
 -  3 pushbuttons.
 -   3 LEDs (any color).
 -   3 x 220 Ohm resistors (current-limiting resistors for LEDs).
 -  10k Ohm resistors (pull-down resistors for buttons).
 -   Jumper wires.
 -    Breadboard.

Circuit Design
 - Each button connects between +5V and a digital input pin (pins 2, 3, and 4).
 -  A 10k Ohm resistor connects between each button pin and GND (pull-down configuration).
 - Each LED connects between a digital output pin (pins 11, 12, and 13) and GND through a 220 Ohm resistor to limit current. Software Design (Arduino Code)

The software consists of:
 - Pin configuration (setup() function): initializing LED pins as OUTPUT and button pins as INPUT.
 - Main loop (loop() function):
 - Reading the state of each button using digitalRead().
 - Setting the corresponding LED state with digitalWrite().

The code is structured to continuously monitor the buttons and immediately respond to any press or release action.

 ## Conclusion

This project effectively demonstrates how to integrate multiple digital inputs and outputs using Arduino. It reinforces core concepts of electronics Digital signal reading and writing, using pull-down resistors to stabilize inputs, protecting LEDs with current-limiting resistors, structuring clear and maintainable code for responsive control.
