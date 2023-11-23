#include <stdio.h>
#include <stdio_ext.h>

#define LIM_ALUMNOS 5

typedef char us;
typedef struct {
  us Nombre[30];
  us Apellido[30];
  int Promedio;
  int Edad;
  int Anio;
} Alumnos;

void PedidaDatos(Alumnos Al[]);

int main(void) {
  Alumnos Al[LIM_ALUMNOS];
  int eleccion = 1;
  int i = 0;
  
  for (i = 0; i < LIM_ALUMNOS; i++) {
    printf("Ingrese los datos del alumno:\n");
    printf("Nombre: ");
    scanf("%s", Al[i].Nombre);
    printf("Apellido: ");
    scanf("\n %s", Al[i].Apellido);
    printf("Promedio: ");
    scanf("%d", &Al[i].Promedio);
    printf("Edad: ");
    scanf("%d", &Al[i].Edad);
    printf("Año: ");
    scanf("%d", &Al[i].Anio);
    printf("1 para continuar, 0 para finalizar el programa \n");
    scanf("%d", &eleccion);
    if (eleccion != 1)
      break;
  }
  PedidaDatos(Al);
  return 0;
}

void PedidaDatos(Alumnos Al[]) {
  int datos, Alum;
  printf("Elija el alumno:\n");
  scanf("%d", &Alum);

  printf("Nombre: %s\n", Al[Alum-1].Nombre);
  printf("Apellido: %s\n", Al[Alum-1].Apellido);
  printf("Promedio: %d\n", Al[Alum-1].Promedio);
  printf("Edad: %d\n", Al[Alum-1].Edad);
  printf("Año: %d\n", Al[Alum-1].Anio);

  if(Alum>LIM_ALUMNOS)printf("No es un alumno valido");
  }
