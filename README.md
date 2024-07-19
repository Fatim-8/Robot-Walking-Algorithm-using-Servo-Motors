
# Robot-Walking-Algorithm-using-Servo-Motors


This algorithm will control the movement of the servo motors located in the robot's legs, which will work together to generate a motion pattern similar to human walking.


~~~
#include <Servo.h>

// Declaring variables for the 6 servo motors
Servo servo1, servo2, servo3, servo4, servo5, servo6;

// Defining the pins for each servo motor
int servo1_pin = 2;
int servo2_pin = 3;
int servo3_pin = 4;
int servo4_pin = 5;
int servo5_pin = 6;
int servo6_pin = 7;

void setup() {
  // Attaching each servo motor to its respective pin
  servo1.attach(servo1_pin);
  servo2.attach(servo2_pin);
  servo3.attach(servo3_pin);
  servo4.attach(servo4_pin);
  servo5.attach(servo5_pin);
  servo6.attach(servo6_pin);
}

void loop() {
  // Commanding the servo motors to move to different positions
  moveServos(0, 30, 60, 90, 120, 150); // Setting the positions
  delay(1000); // Pausing for 1 second

  // Commanding the servo motors to move to different positions
  moveServos(180, 150, 120, 90, 60, 30); // Setting the positions
  delay(1000); // Pausing for 1 second
}

void moveServos(int pos1, int pos2, int pos3, int pos4, int pos5, int pos6) {
  // Moving each servo motor to the specified position
  servo1.write(pos1);
  servo2.write(pos2);
  servo3.write(pos3);
  servo4.write(pos4);
  servo5.write(pos5);
  servo6.write(pos6);
}
~~~
