# #5 Techno-Crafts with Arduino
<div style="text-align: right;">
    4I24 中川 寛之
</div>  

## Purpose of the Experiment

The primary goal of this technical work is for participants to understand the fundamental principles of how electronic devices are developed.  
By using an Arduino microcontroller, the exercises aim to provide a hands-on experience in electronic control, demonstrating the relationship between hardware (inputs/outputs) and software (programs).

## Activities and Methods

### Assembling a Basic Buzzer Circuit

- **Method:**
    - A circuit was assembled connecting a buzzer and a resistor to a "digital No. 12 pin" (D12) on an Arduino Duemilanove board, which was fixed to a breadboard.
    - The Arduino was connected to a PC via a USB cable for power and programming.
    - A program was written in the Arduino IDE to make the buzzer turn on for 1000 ms and off for 1000 ms repeatedly, using a frequency of 440 Hz.
    - This was later modified to play a simple "Do-Re-Mi" scale by changing the frequency values in the code.

### Displaying Characters on a Liquid Crystal Display (LCD)

- **Method:**
    - The existing circuit was expanded by adding a 16x2 character LCD.
    - The LCD was wired to multiple digital pins on the Arduino (pins 2 through 7).
    - A new program was created that utilized the LiquidCrystal.h library to initialize the display and print a default message.
    - The program was designed to receive character data from the PC's "serial monitor" and display it on the LCD.

### Building a Distance Measuring Device (Rangefinder)

- **Method:**
    - **Sensor Characterization:**
        - The characteristics of an infrared distance sensor were investigated.
        - The sensor was powered by the Arduino's 5V and GND pins.
        - A digital multimeter was used to measure the sensor's analog output voltage (Vo) when an object was placed at specific distances, from 10 cm to 70 cm.
    - **Data Analysis:**
        - The collected voltage and distance data were plotted on a graph to establish their relationship.
        - This relationship was approximated by an inverse proportional equation, v = d / l, to convert voltage readings into distance.
    - **Arduino as a Voltmeter:**
        - The digital multimeter was removed, and the sensor's output (Vo) was connected to an analog input pin (A0) on the Arduino.
        - A program was written to read the analog value (0-1023) and convert it into a voltage (0-5V), displaying the result on the LCD.
    - **Rangefinder Creation:**
        - The program was modified to incorporate the previously derived equation (l = d / v) to convert the measured voltage into distance in centimeters, which was then displayed on the LCD.
    - **Adding an Alarm Function:**
        - As a final step, conditional logic (if statements) was added to the program.
        - This made the buzzer sound an alarm (e.g., at 880 Hz) if the measured distance fell below a specified threshold, such as 30 cm.
        - Further application examples suggested changing the alarm's frequency or displaying a "caution!"