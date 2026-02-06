#include <Servo.h>

Servo palang;

int trigPin = 9;
int echoPin = 10;
int servoPin = 6;

long durasi;
int jarak;

void setup() {
  palang.attach(servoPin);

  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);

  Serial.begin(9600);
}

void loop() {
  
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  
  durasi = pulseIn(echoPin, HIGH);
  jarak = durasi * 0.034 / 2;

  
  if (jarak <= 10) {
    palang.write(90);  
  } else {
    palang.write(0);    
  }

  delay(2000);
}
