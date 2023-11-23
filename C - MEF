#define RETARDO 40
#define LED_ROJO 7
#define LED_VERDE 3
#define PULSADOR 9

void debounceFSM_init();   // debe cargar el estado inicial
void debounceFSM_update();

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

void setup(){
  pinMode(PULSADOR, INPUT);
  pinMode(LED_ROJO, OUTPUT);
  pinMode(LED_VERDE, OUTPUT);
  debounceFSM_init();
  Serial.begin(9600);
}

void loop(){
  debounceFSM_update();
  delay(5);
}

void debounceFSM_init(){
  estadoactual = BUTTON_UP;
}

void debounceFSM_update(){
  static unsigned long pr…
