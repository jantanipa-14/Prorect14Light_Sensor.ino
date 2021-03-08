# Prorect14Light_Sensor.ino
Cose Light-Sensor
int ldr = A0;
int led = 8;

void setup()
{
  Serial.begin(9600);
  
  pinMode(ldr, INPUT);
  pinMode(led, OUTPUT);
}

void loop()
{
  int ldrVal = analogRead(ldr);

  Serial.println("LDR Sensor");
  Serial.println(ldrVal);

  if (ldrVal > 500) {
    digitalWrite(led, HIGH);
  } else {
    digitalWrite(led, LOW);
  }

  delay(500);
}
