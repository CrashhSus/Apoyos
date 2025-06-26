import random

participantes = []

print("Registro de 10 participantes:")
for i in range(1, 11):
    nombre = input(f"Ingrese el nombre del participante #{i}: ")
    participantes.append(nombre)

ganadores = random.sample(participantes, 5)

premios = [
    "1.000.000 de pesos",
    "500.000 pesos",
    "250.000 pesos",
    "100.000 pesos",
    "una medalla"
]

print("\nResultados del concurso:")
for i, ganador in enumerate(ganadores):
    print(f"Puesto #{i+1}: {ganador} gana {premios[i]}")

no_ganadores = [p for p in participantes if p not in ganadores]

print("\nParticipantes que no ganaron:")
for p in no_ganadores:
    print(f"{p} Gracias por participar :D")
