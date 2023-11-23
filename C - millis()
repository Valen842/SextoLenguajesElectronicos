#define LED 10

unsigned long time;

void ONOFF(bool*); //pasaré un puntero

bool flag = false; //creo una variable flag

void setup() {
  pinMode(LED, OUTPUT);
  time = millis();
  Serial.begin(9600); //Para chequear el funcionamiento
}

void loop() {
  ONOFF(&flag);//apuntare al flag
  delay(5);
}

void ONOFF(bool* flagPtr) { //flag=flagPtr
  Serial.println(*flagPtr); //Para chequear el funcionamiento
  if (millis() - time >= 2000) { //Cada 2 segundos, la diferencia, se modificará
    time = millis(); //recargo la variable time
    if (*flagPtr == false) {
      digitalWrite(LED, HIGH);
      *flagPtr = true;
    } else {
      digitalWrite(LED, LOW);
      *flagPtr = false;
    }
  }
}
