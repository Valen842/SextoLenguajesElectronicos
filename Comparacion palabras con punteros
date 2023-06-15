#include <stdio.h>
#include <stdio_ext.h>

#define MAX_TAMANIO 100

void comparacion(char texto1[], char texto2[]);

int main(){
  char texto1[MAX_TAMANIO], texto2[MAX_TAMANIO];
  printf("Introduzca la primer palabra\n");
  scanf("%s", texto1);
  printf("Introduzca la segunda palabra\n");
  scanf("%s", texto2);
  comparacion(texto1, texto2);
}

void comparacion(char texto1[], char texto2[]){
  char *puntexto1 = &texto1[0];
  char *puntexto2 = &texto2[0];
  int letra;
  char flag;
  
  for (letra=0; *puntexto1!='\0'; puntexto1++, puntexto2++)
  {
    if(*puntexto1==*puntexto2){
      flag = 0;
    }else{
      flag = 1;
      break;
    }  
  }
  
  if (flag==1) printf("%s no es igual a %s", texto1, texto2);
  else if (flag==0) printf("%s es igual a %s", texto1, texto2);
}


/* notas
#include <stdio.h>

char *pchar; //puntero(pchar) en dirección de char

int main(void) {
  char var=3; //var es direccion de memoria
  char var2=8; //var es la segunda direccion de memoria
  char *pchar=&var; //asigna la dirección de var al puntero
  printf("Lugar var1: 0x%x\n", pchar); //lugar de memoria
  printf("Valor var1: %d\n", *pchar); //valor de el lugar de memoria
  pchar=&var2; //cambio la dirección
  printf("\nLugar var2: 0x%x\n", pchar); //lugar de memoria
  printf("Valor var2: %d\n", *pchar); //valor de el lugar de memoria
  return 0;
}
*/
