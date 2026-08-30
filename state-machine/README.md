# State Machine Module

## Wiring Diagram
<img width="721" height="437" alt="image" src="https://github.com/user-attachments/assets/ddd05278-f5f7-4d3c-90b7-3adbb875e7f8" />

## Moore State Machine
<img width="1190" height="345" alt="image" src="https://github.com/user-attachments/assets/6db88b4c-3d4a-4ce3-8c7e-e10a4c81ad53" />

* The Architecture used for the state machine module was a Moore State machine, and the encoding was one hot encoding. In order to move between states there are two inputs up and down, these are then used with digital logic to interpret whether they are pressed or not and depending on which state the machine is currently at, the next state will be determined.

* Once the machine entered a state a 5 bit number corresponding to the state was sent to the PWM, and two 4 bit signals were sent to the two digits to display the current duty cycle that the PWM was producing. Below are the three tables specifying the corresponding bit signals for the PWM module and the BCD-7 Segment Display module

## PWM Signal
| State | Binary Number | Duty Cycle | Displayed Number |
|---|---|---|---|
| s0 | 00000 | 0% | 00 |
| s1 | 00101 | 16.1% | 15 |
| s2 | 01010 | 32.3% | 30 |
| s3 | 01110 | 45.2% | 45 |
| s4 | 10011 | 61.3% | 60 |
| s5 | 11000 | 77.4% | 80 |
| s6 | 11101 | 93.5% | 95 |

## BCD to 7 Segment Display
* The signal used for the BCD-7 Segment Display module is composed of 4 bits representing a number from 0 to 9. However as observed by the table values certain digits are repeated for the display number in some states, allowing for certain bits to be tied to a specific value since regardless of the state they will remain the same.

### Tens Digit Display

| State | 4-bit Binary | Displayed Digit |
|---|---|---|
| s0 | 0000 | 0 |
| s1 | 0001 | 1 |
| s2 | 0011 | 3 |
| s3 | 0100 | 4 |
| s4 | 0110 | 6 |
| s5 | 1000 | 8 |
| s6 | 1001 | 9 |

### Ones Digit Display

| State | 4-bit Binary | Displayed Digit |
|---|---|---|
| s0 | 0000 | 0 |
| s1 | 0101 | 5 |
| s2 | 0000 | 0 |
| s3 | 0101 | 5 |
| s4 | 0000 | 0 |
| s5 | 0000 | 0 |
| s6 | 0101 | 5 |
