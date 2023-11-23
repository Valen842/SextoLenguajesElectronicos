#include "stdio.h"
#include "stdio_ext.h"

void PasajeCelcius (int*);
void PasajeKelvin(int*);

int main(void){
  
  int Temp;
  char Medicion;
  int *p = &Temp;
  __fpurge(stdin);
  printf("Coloque la temperatura ambiente actual:\n");
  __fpurge(stdin);
  scanf("%d", &Temp);
  __fpurge(stdin);
  printf("Indique:\nSi es Celcius con C\nSi es Kelvin con K\n");
  __fpurge(stdin);
  scanf("%c", &Medicion);
  __fpurge(stdin);
  switch(Medicion){
    case('K'|'k'):
      PasajeKelvin(p);
      break;
    case('C'|'c'):
      PasajeCelcius(p);
      break;
  }
}


void PasajeKelvin(int *p){
  *p = *p - 273.15;
  printf("El valor en Celcius es: %d\n", *p);
  
}

void PasajeCelcius(int *p){
  *p = *p + 273.15;
  printf("El valor en Kelvin es: %d\n", *p);
}
