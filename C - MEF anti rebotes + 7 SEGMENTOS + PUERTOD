//MEF PULSADOR
#define RETARDO 40
#define LED_ROJO 9
#define LED_VERDE 10
#define PULSADOR 8


void debounceFSM_init();
void debounceFSM_update();


void buttonPressed();
void buttonReleased();


void inicializacion_display (void);


typedef enum{
  BUTTON_UP,
  BUTTON_FALLING,
  BUTTON_DOWN,
  BUTTON_RISING,
} debounceState_t;

debounceState_t estadoactual;

//DISPLAY
char numero[16]{
  B10000000, // 0
  B11110010, // 1
  B01001000, // 2
  B01100000, // 3
  B00110010, // 4
  B00100100, // 5
  B00000100, // 6
  B11110000, // 7
  B00000000, // 8
  B00110000, // 9
  B01000000, // a
  B00000110, // b
  B10001100, // c
  B01000010, // d
  B00001000, // e
  B00011100  // f
};

int cuentaNum = 1;

void setup(){
 
  pinMode(PULSADOR, INPUT);
  pinMode(LED_ROJO, OUTPUT);
  pinMode(LED_VERDE, OUTPUT);
  DDRD=B11111111;
  inicializacion_display();
  debounceFSM_init();
}

void loop(){
  debounceFSM_update();
}



void debounceFSM_init(){
  estadoactual = BUTTON_UP;
}

void debounceFSM_update(){
  static unsigned long previo = millis();
 
  switch (estadoactual){
    case BUTTON_UP:
      if (digitalRead(PULSADOR) == LOW){
        estadoactual = BUTTON_FALLING;
        previo = millis();
      }
   break;
   
    case BUTTON_DOWN:
      if (digitalRead(PULSADOR) == HIGH){
        estadoactual = BUTTON_RISING;
        previo = millis();
      }
    break;
    case BUTTON_FALLING:
        if (millis()-previo>=RETARDO){
          if(digitalRead(PULSADOR)==LOW){
            buttonPressed();
            estadoactual = BUTTON_DOWN;
          }else{
            estadoactual = BUTTON_UP;
          }
        }
    break;
    case BUTTON_RISING:
        if (millis()-previo>=RETARDO){
          if(digitalRead(PULSADOR)==HIGH){
            buttonReleased();
            estadoactual = BUTTON_UP;
          }else{
            estadoactual = BUTTON_DOWN;
          }
        }
    break;
    }
}

void buttonPressed(){
  digitalWrite(LED_VERDE, HIGH);
  digitalWrite(LED_ROJO, LOW);
  PORTD = numero[cuentaNum];
  if (cuentaNum == 15) cuentaNum = 0;
  else cuentaNum++;
 
}

void buttonReleased(){
  digitalWrite(LED_VERDE, LOW);
  digitalWrite(LED_ROJO, HIGH);
}

void inicializacion_display (void){
  PORTD = B01111110;
}
