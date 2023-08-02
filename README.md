# connect_two_arduino

link to tinkercad "https://www.tinkercad.com/things/8Dp0TSqHTXA-two-arduino/editel"

the first arduni send digital number to second arduno by use TX TO RX

const int inPin = 3;

void setup()
{
  pinMode(inPin, INPUT);
  Serial.begin(9600);
}

void loop()
{
  Serial.print( digitalRead(inPin));
  delay(1000);
}

in here the second arduni Receiver the number and execute then the led is open

const int inPin = 3;

const int OUT_PIN = 2;

int buttonState ;

void setup()
{
  pinMode(OUT_PIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  if(Serial.available() == 1) {
    buttonState = bitRead(Serial.read(), 0);
  }
  digitalWrite(OUT_PIN, buttonState);
  delay(1000);
}

void loop()
{
  Serial.print( digitalRead(inPin));
  delay(1000);
}
