int m1 = 4;
int m2 = 3;

int m3 = 6;
int m4 = 5;

int m5 = 10;
int m6 = 9;

int m7 = 13;
int m8 = 12;

int mspeed1 = 2;
int mspeed2 = 7;
int mspeed3 = 8;
int mspeed4 = 11;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println(" START ");  
  
  pinMode(m1, OUTPUT);
  pinMode(m2, OUTPUT);
  pinMode(m3, OUTPUT);
  pinMode(m4, OUTPUT);
  pinMode(m5, OUTPUT);
  pinMode(m6, OUTPUT);
  pinMode(m7, OUTPUT);
  pinMode(m8, OUTPUT);
}

void loop() {
  //TO CHECK AND EXECUTE ONLY IF BLUETOOTH IS CONNECTED
  if(Serial.available() > 0)
  {
    char data;
    data = Serial.read();
    Serial.write(Serial.read());

    switch (data)
    {
      
      case '1': //TO MOVE FORWARD
          digitalWrite(m1, HIGH);
          digitalWrite(m2, LOW);
          analogWrite(mspeed1, 255);

          digitalWrite(m3, HIGH);
          digitalWrite(m4, LOW);
          analogWrite(mspeed2, 255);

          digitalWrite(m5, HIGH);
          digitalWrite(m6, LOW);
          analogWrite(mspeed3, 255);

          digitalWrite(m7, HIGH);
          digitalWrite(m8, LOW);
          analogWrite(mspeed4, 255);
        break;
        
      case '2': //TO REVERSE
          digitalWrite(m1, LOW);
          digitalWrite(m2, HIGH);
          analogWrite(mspeed1, 255);

          digitalWrite(m3, LOW);
          digitalWrite(m4, HIGH);
          analogWrite(mspeed2, 255);

          digitalWrite(m5, LOW);
          digitalWrite(m6, HIGH);
          analogWrite(mspeed3, 255);

          digitalWrite(m7, LOW);
          digitalWrite(m8, HIGH);
          analogWrite(mspeed4, 255);
        break;
        
      case '3': //FORWARD LEFT
          digitalWrite(m1, HIGH);
          digitalWrite(m2, LOW);
          analogWrite(mspeed1, 255);

          digitalWrite(m3, HIGH);
          digitalWrite(m4, LOW);
          analogWrite(mspeed2, 255);

          digitalWrite(m5, LOW);
          digitalWrite(m6, HIGH);
          analogWrite(mspeed3, 225);

          digitalWrite(m7, LOW);
          digitalWrite(m8, HIGH);
          analogWrite(mspeed4, 225);
        break;
        
      case '4': //FORWARD RIGHT
          digitalWrite(m1, LOW);
          digitalWrite(m2, HIGH);
          analogWrite(mspeed1, 225);

          digitalWrite(m3, LOW);
          digitalWrite(m4, HIGH);
          analogWrite(mspeed2, 225);

          digitalWrite(m5, HIGH);
          digitalWrite(m6, LOW);
          analogWrite(mspeed3, 225);

          digitalWrite(m7, HIGH);
          digitalWrite(m8, LOW);
          analogWrite(mspeed4, 225);
        break;
               
      default: //If invalid input is received by the bluetooth module then both motors turn off
          digitalWrite(m1, LOW);
          digitalWrite(m2, LOW);
          analogWrite(mspeed1, 0);

          digitalWrite(m3, LOW);
          digitalWrite(m4, LOW);
          analogWrite(mspeed2, 0);

          digitalWrite(m5, LOW);
          digitalWrite(m6, LOW);
          analogWrite(mspeed3, 0);

          digitalWrite(m7, LOW);
          digitalWrite(m8, LOW);
          analogWrite(mspeed4, 0);
    }
  }
}
