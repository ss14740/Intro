Task 1:
P5 Code:
https://editor.p5js.org/insiyam/sketches/aZKDbrgGR

Arduino:

const int POT = A0;
const int PR = A1;

void setup() {
  Serial.begin(9600);

}

void loop() {

 // send information to p5
  int potValue = analogRead(POT);
  int prValue = analogRead(PR);
  Serial.print(potValue);
  Serial.print(",");
  Serial.println(prValue);

}


Task 2:
P5 Code:
https://editor.p5js.org/batoxpr/sketches/iUUjxHgDT

Arduino:

const int LED = 3;
void setup() {
  Serial.begin(9600);
  pinMode(LED, OUTPUT);
  while (Serial.available() <= 0) {
    Serial.println("hello"); // send a starting message
    delay(300); //wait 1/3 second
  }
}

void loop() {

  // read information from p5
  if (Serial.available() > 0) {
    int ledValue = Serial.read();
    if (ledValue == 0) {
      analogWrite(LED, ledValue);
    } else {
      analogWrite(LED,ledValue);
    }  
  }
  }
