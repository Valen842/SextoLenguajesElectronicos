#include "stdio.h"
#include "stdio_ext.h"

void PasajePorValor (int);
void PasajePorReferencia (int*);

int main(void){
  int a = 1;
  int b = 1;
  int *p = &b;
  PasajePorValor(a);
  printf("Salida Main A: %d\n\n", a);
  PasajePorReferencia(&b);
  printf("Salida Main B: %d\n", b);
}

void PasajePorValor(int a)
{
  a++;
  printf("Salida Pasaje por valor: %d\n", a);
}

void PasajePorReferencia (int *b)
{
  (*b)++;
  //*p=*p+1;
  printf("Pasaje por Referencia: %d\n", *b);
}
