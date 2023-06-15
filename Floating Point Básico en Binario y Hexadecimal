#include <stdio.h>
typedef unsigned char usc;

union{
  float NumeroDecimal;
  usc FloatingPoint[4];
}numeros;

int hexadecimal(void);
void binario(void);

int main(void) {
  printf("Ingresar el número:\n");
  scanf("%f", &numeros.NumeroDecimal);
  hexadecimal();
  binario();
  return 0; 
}
 
int hexadecimal(void){
  printf("0x: %0.2x", numeros.FloatingPoint[3]);
  printf("%.2x", numeros.FloatingPoint[2]);
  printf("%.2x", numeros.FloatingPoint[1]);
  printf("%.2x\n", numeros.FloatingPoint[0]);
  return 0;
}
void binario(void){
  printf("0b: ");
  for(int j = 3; j!=-1; j--){
    for(int i=7 ; i>1;i--){
      printf("%d", (numeros.FloatingPoint[j] >> i)&01); 
    }
  }
}
