'''
VALENTINO BISBANO SIMULACION MATERIAS 6 AÑOS
PYTHON CODE
'''
import random

# Crear una lista de nombres de alumnos
nombres_alumnos = [
  "Abril",
  "Agustina",
  "Amiel",
  "Bautista",
  "Candela",
  "Diego",
  "Felicitas",
  "Fran",
  "Gabo",
  "Gian",
  "Juan",
  "Julieta",
  "Lucas", 
  "Maite",
  "Nacho",
  "Pedro",
  "Pilar",
  "Tomas",
  "Santiago",
  "Sofia"
]

# Crear un diccionario para almacenar datos de los alumnos
alumnos = {
    nombre: {
        "materias": {
            "geografia": [],
            "historia": [],
            "matematicas": []
        },
        "inasistencias": []
    }
    for nombre in nombres_alumnos
}

# Función para generar notas aleatorias y registrar inasistencias
def generar_notas_inasistencias():
    probabilidades_notas = [0.05] * 3 + [0.2] * 4 + [0.75] * 4
    probabilidades_inasistencias = [0.5] * 4 + [0.9] * 15 + [0.05] * 10
  
    inasistencias = random.choices(range(29), weights = probabilidades_inasistencias)[0]
    
    notas_geografia = random.choices(range(11), weights=probabilidades_notas)[0]
    notas_historia = random.choices(range(11), weights=probabilidades_notas)[0]
    notas_matematicas = random.choices(range(11), weights=probabilidades_notas)[0]
    
    return {
        "geografia": notas_geografia,
        "historia": notas_historia,
        "matematicas": notas_matematicas,
        "inasistencias": inasistencias
    }

# Simulación de la trayectoria escolar durante 6 años
for _ in range(7):
    for nombre, datos in alumnos.items():
        # Generar notas e inasistencias para el año actual
        datos_año = generar_notas_inasistencias()
        datos["materias"]["geografia"].append(datos_año["geografia"])
        datos["materias"]["historia"].append(datos_año["historia"])
        datos["materias"]["matematicas"].append(datos_año["matematicas"])
        datos["inasistencias"].append(datos_año["inasistencias"])

# Calcular promedio general y determinar aprobados
for nombre, datos in alumnos.items():
    promedio_general = (sum(datos["materias"]["geografia"]) + sum(datos["materias"]["historia"]) + sum(datos["materias"]["matematicas"])) / 21.0
    datos["promedio_general"] = promedio_general
    aprobado = promedio_general >= 7.0 and max(datos["inasistencias"]) <= 20
    datos["aprobado"] = aprobado

# Mostrar resultados en el formato deseado
for nombre, datos in alumnos.items():
    print(f"Nombre: {nombre}")
    print(f"  Promedio General: {datos['promedio_general']:.2f}")
    if ((max(datos['inasistencias']) > 20) and (datos["promedio_general"] < 7.0) or ((max(datos['inasistencias']) > 20) and (datos["promedio_general"] >= 7.0))):
      print(f"  Inasistencias: LIBRE, {max(datos['inasistencias'])}")
      print("  Estado: REPITE \n")
    elif (max(datos['inasistencias']) <= 20) and (datos["promedio_general"] < 7.0):
      print(f"  Inasistencias: {max(datos['inasistencias'])}")
      print("  Estado: REPITE \n") 
    elif (max(datos['inasistencias']) <= 20) and (datos["promedio_general"] >= 7.0):
      print(f"  Inasistencias: {max(datos['inasistencias'])}")
      print("  Estado: Egresa \n")
