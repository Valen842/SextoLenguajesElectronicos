/*
VALENTINO BISBANO C++ CODE
USES CLASSES + STRUCTURES
*/

#include <iostream>
using namespace std;

enum Lado {
  VERTICAL,
  HORIZONTAL,
  PROFUNDIDAD
};

class Cubo {
  private:
    int alto, ancho, profundidad;
  
  public:
    void setDimension(Lado lado, int size);
    int getVolumen();
    int getPerimetro();
  };
  
  void Cubo::setDimension(Lado lado, int size) {
    while (size <= 0) {
      cout << "Error: El tamaño debe ser mayor que cero. Ingrese nuevamente: ";
      cin >> size;
    }
    
    switch (lado) {
      case VERTICAL:
        alto = size;
        break;
      case HORIZONTAL:
        ancho = size;
        break;
      case PROFUNDIDAD:
        profundidad = size;
        break;
    }
}

int Cubo::getVolumen() {
  return alto * ancho * profundidad;
}

int Cubo::getPerimetro() {
  return 4 * (alto + ancho + profundidad);
}

int main() {
  Cubo cubo1;
  int alto, ancho, profundidad;

  cout << "Ingrese el alto: ";
  cin >> alto;
  cubo1.setDimension(VERTICAL, alto);

  cout << "Ingrese el ancho: ";
  cin >> ancho;
  cubo1.setDimension(HORIZONTAL, ancho);

  cout << "Ingrese la profundidad: ";
  cin >> profundidad;
  cubo1.setDimension(PROFUNDIDAD, profundidad);

  cout << "El volumen es: " << cubo1.getVolumen() << "\n";
  cout << "El perimetro es: " << cubo1.getPerimetro() << "\n";

  return 0;
}
