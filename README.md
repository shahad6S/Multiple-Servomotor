# ThinkerCode
// C++ code
//
#include <Servo.h>

int servoValue = 0;

int servoValue2 = 0;

int servoValue3 = 0;

int servoValue4 = 0;

int servoValue5 = 0;

Servo servo_9;

Servo servo_10;

Servo servo_11;

Servo servo_6;

Servo servo_5;

void setup()
{
  pinMode(A0, INPUT);
  servo_9.attach(9, 500, 2500);

  pinMode(A1, INPUT);
  servo_10.attach(10, 500, 2500);

  pinMode(A2, INPUT);
  servo_11.attach(11, 500, 2500);

  pinMode(A3, INPUT);
  servo_6.attach(6, 500, 2500);

  pinMode(A4, INPUT);
  servo_5.attach(5, 500, 2500);

}

void loop()
{
  servoValue = analogRead(A0);
  servoValue = map(servoValue, 0, 1023, 0, 90);
  servo_9.write(servoValue);

  servoValue2 = analogRead(A1);
  servoValue2 = map(servoValue2, 0, 1023, 0, 90);
  servo_10.write(servoValue2);

  servoValue3 = analogRead(A2);
  servoValue3 = map(servoValue3, 0, 1023, 0, 90);
  servo_11.write(servoValue3);

  servoValue4 = analogRead(A3);
  servoValue4 = map(servoValue4, 0, 1023, 0, 90);
  servo_6.write(servoValue4);

  servoValue5 = analogRead(A4);
  servoValue5 = map(servoValue5, 0, 1023, 0, 90);
  servo_5.write(servoValue5);
  delay(10); // Delay a little bit to improve simulation performance
}
