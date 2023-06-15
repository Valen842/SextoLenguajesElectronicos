#include <stdio.h>

typedef unsigned int us;

typedef union {
  float flotante;
  struct{
    // uint8_t = us
    us mantisa : 23;
    us exponente : 8;
    us signo : 1;
  } bin;
} Float;

void Flotante();
void MascaraBinaria(int, int);
 
int main()
{
  Float var;
  printf("Ingrese su número: \n ");
  scanf("%f",&var.flotante);
  Flotante(var);
  return 0;
}

void MascaraBinaria(valor, tamanio){
  for (int ini = tamanio - 1; ini >= 0; ini--){
    if ((valor >> ini) & 1)printf("1");
    else printf("0");
  }
}

void Flotante(Float var){
  printf("0b: %d ", var.bin.signo);
  MascaraBinaria(var.bin.exponente, 8);
  printf(" ");
  MascaraBinaria(var.bin.mantisa, 23);
  printf("\n");
}
