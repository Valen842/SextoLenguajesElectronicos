//MEF PULSADOR

#define RETARDO 40
#define LED_ROJO 12
#define LED_VERDE 10
#define PULSADOR 13


void debounceFSM_init();// debe cargar el estado inicial
void debounceFSM_update();	// debe leer las entradas, resolver la lógica de

// transición de estados y actualizar las salidas
void buttonPressed();// debe invertir el estado del LED1
void buttonReleased();// debe invertir el estado del LED2 

typedef enum{
  BUTTON_UP,
  BUTTON_FALLING,
  BUTTON_DOWN,
  BUTTON_RISING,
} debounceState_t;

debounceState_t estadoactual;


//DISPLAY

#define displayA 7
#define displayB 6
#define displayC 3
#define displayD 4
#define displayE 5
#define displayF 8
#define displayG 9

void mostrarNumero(int);

int cuentaNum = 0; //valor de MostrarNumero


//Funciones de cuenta de números
void numero0(void);
void numero1(void);
void numero2(void);
void numero3(void);
void numero4(void);
void numero5(void);
void numero6(void);
void numero7(void);
void numero8(void);
void numero9(void);
void numeroA(void);
void numeroB(void);
void numeroC(void);
void numeroD(void);
void numeroE(void);
void numeroF(void);

void setup(){
  
  //DYSPLAY seteo
  pinMode(displayA, OUTPUT);
  pinMode(displayB, OUTPUT);
  pinMode(displayC, OUTPUT);
  pinMode(displayD, OUTPUT);
  pinMode(displayE, OUTPUT);
  pinMode(displayF, OUTPUT);
  pinMode(displayG, OUTPUT);

  
  //MEF PULSADOR seteo
  pinMode(PULSADOR, INPUT);
  pinMode(LED_ROJO, OUTPUT);
  pinMode(LED_VERDE, OUTPUT);
  debounceFSM_init();
  Serial.begin(9600);
  
  //Tinkercad espera un ciclo para iniciar su cuenta, debemos inicializar
  numero0();
}

void loop(){
  debounceFSM_update();
  delay(5);
}


//MEF PULSADOR
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
          	mostrarNumero(cuentaNum);
        }
    	break;
    
    case BUTTON_DOWN:
    	if (digitalRead(PULSADOR) == HIGH){
            estadoactual = BUTTON_RISING;
            previo = millis();
            mostrarNumero(cuentaNum);
        }
    	break;
    
    case BUTTON_FALLING:
        if (millis()-previo>=RETARDO){
          if(digitalRead(PULSADOR)==LOW){
            buttonPressed();
            estadoactual = BUTTON_DOWN;
            cuentaNum++; //sumo a la cuenta para modificar el numero mostrado
          }else{
            estadoactual = BUTTON_UP;
            mostrarNumero(cuentaNum);
          }
        }
    	break;
    	
    case BUTTON_RISING:
        if (millis()-previo>=RETARDO){
          if(digitalRead(PULSADOR)==HIGH){
            buttonReleased();
            estadoactual = BUTTON_UP;
          } else{
            estadoactual = BUTTON_DOWN;
            mostrarNumero(cuentaNum);
          }
        }
    	break;
  }
}

void buttonPressed(){
 digitalWrite(LED_VERDE, HIGH);
 digitalWrite(LED_ROJO, LOW);
}

void buttonReleased(){
 digitalWrite(LED_VERDE, LOW);
 digitalWrite(LED_ROJO, HIGH); 
}




//DISPLAY
void mostrarNumero(int cuentaNum){ //veo la cuenta previamente hechay de
  //forma podemos ir relacionando la suma con las funciones
  switch(cuentaNum) {
    case 0:
      numero0();
      break;
    case 1:
      numero1();
      break;
    case 2:
      numero2();
      break;
    case 3:
      numero3();
      break;
	case 4:
      numero4();
      break;
    case 5:
      numero5();
      break;
    case 6:
      numero6();
      break;
    case 7:
      numero7();
      break;
    case 8:
      numero8();
      break;
	case 9:
      numero9();
      break;
    case 10:
      numeroA();
      break;
    case 11:
      numeroB();
      break;
    case 12:
      numeroC();
      break;
    case 13:
      numeroD();
      break;
    case 14:
      numeroE();
      break;
	case 15:
      numeroF();
      break;
    default:
      cuentaNum = 0;
      numero0();
  }
}

//Seteo de los numeros para que dependan de una sola funcion

void numero0(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, LOW);
}

void numero1(){
  digitalWrite(displayA, LOW);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, LOW);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, LOW);
}

void numero2(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, LOW);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, HIGH);
}

void numero3(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, HIGH);
}

void numero4(){
  digitalWrite(displayA, LOW);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, LOW);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numero5(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, LOW);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numero6(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, LOW);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numero7(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, LOW);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, LOW);
}

void numero8(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numero9(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, LOW);
  digitalWrite(displayE, LOW);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numeroA(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, HIGH);
}

void numeroB(){
  digitalWrite(displayA, LOW);
  digitalWrite(displayB, LOW);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numeroC(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, LOW);
  digitalWrite(displayC, LOW);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, LOW);
}

void numeroD(){
  digitalWrite(displayA, LOW);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, HIGH);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, LOW);
  digitalWrite(displayG, HIGH);
}

void numeroE(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, HIGH);
  digitalWrite(displayC, LOW);
  digitalWrite(displayD, HIGH);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}

void numeroF(){
  digitalWrite(displayA, HIGH);
  digitalWrite(displayB, LOW);
  digitalWrite(displayC, LOW);
  digitalWrite(displayD, LOW);
  digitalWrite(displayE, HIGH);
  digitalWrite(displayF, HIGH);
  digitalWrite(displayG, HIGH);
}
