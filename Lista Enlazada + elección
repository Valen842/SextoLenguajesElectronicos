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

  int NumAlum;
  
  alumno1.nombre = "Simon";
  alumno1.apellido = "Vega";
  
  alumno2.nombre = "Marcos";
  alumno2.apellido = "Giovannelli";
  
  alumno3.nombre = "Francisco";
  alumno3.apellido = "Jaime";
  
  alumno4.nombre = "Valentino";
  alumno4.apellido = "Bisbano";

  printf("Ingrese el numero del alumno que desea ver:\n");
  scanf("%i", &NumAlum);

  switch(NumAlum) {

    case 1:
      printf("Nombre del alumno: %s\n" ,p-> nombre); 
      printf("Apellido del alumno: %s\n\n", p->apellido);
      break;
    case 2:
      p = p->siguiente;
      printf("Nombre del alumno: %s\n" ,p-> nombre); 
      printf("Apellido del alumno: %s\n\n", p->apellido);
      break;   
    case 3:
      p = p->siguiente;
      p = p->siguiente;
      printf("Nombre del alumno: %s\n" ,p-> nombre); 
      printf("Apellido del alumno: %s\n\n", p->apellido);
      break;  
    case 4:
      p = p->siguiente;
      p = p->siguiente;
      p = p->siguiente;
      printf("Nombre del alumno: %s\n" ,p-> nombre); 
      printf("Apellido del alumno: %s\n\n", p->apellido);
      break;  
    default:
     printf("No es un numero valido");
  }
}
