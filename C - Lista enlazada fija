#include <stdio.h>
typedef unsigned int us;
typedef char usc;

struct alumnos{
  usc* nombre; 
  usc* apellido;
  us edad;
  struct alumnos *siguiente;
}alumno1, alumno2, alumno3, alumno4;

int main(){
  struct alumnos *p=&alumno1; 
  alumno1.siguiente=&alumno2;
  alumno2.siguiente=&alumno3;
  alumno3.siguiente=&alumno4;
  alumno4.siguiente=NULL;
  
  alumno1.nombre = "Simon";
  alumno1.apellido = "Vega";
  alumno2.nombre = "Marcos";
  alumno2.apellido = "Giovannelli";
  
  alumno3.nombre = "Francisco";
  alumno3.apellido = "Jaime";
  
  alumno4.nombre = "Valentino";
  alumno4.apellido = "Bisbano";
  
  do
  {
    printf("Nombre del alumno: %s\n" ,p-> nombre); 
    printf("Apellido del alumno: %s\n\n", p->apellido);
    p = p->siguiente;
  }while(p->siguiente!=NULL);
  
  printf("Nombre del alumno: %s\n", p->nombre);
  printf("Apellido del alumno: %s\n", p->apellido);
  
  return 0;
}
