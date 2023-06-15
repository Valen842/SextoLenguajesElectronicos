//Punteros a estructuras explicacion
#include <stdio.h>

struct datos{
  int a;
  int b;
}estructura;

int main(void) {
  struct datos *p=&estructura; // puntero q apunta a estructura
  estructura.a=10; //valor de a modificado
  printf("Valor de a en estructura: %d\n", estructura.a );
  printf("Valor de a por estructura por el puntero: %d\n", (*p).a);
  printf("Valor de a por estructura por el puntero: %d\n\n", p->a);
  estructura.b=8;
  p->b=15; //modificamos valor de b mediante puntero
  printf("Valor de b en estructura: %d\n", estructura.b);
  printf("Valor de b por estructura por el puntero: %d\n\n", p->b);
  return 0;
}
