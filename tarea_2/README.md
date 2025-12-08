# Reto 1: Simular el comportamiento de la tortuga usando solo print() e input()
Este programa dibuja una flecha usando guiones y el símbolo >. 

```python
from re import L

pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):     
    print("-", end="")

print(">")
```

# Reto 2: Tortuga bajando
Dibuja una flecha vertical usando líneas hacia abajo y una punta al final.

pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):
    print("|")

print("V")

# Reto 3: Girar y dibujar usando solo print() e input()
Dibuja una flecha que primero va a la derecha y luego baja.

from re import L

pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):  
    print("-", end="")

print(">")

for i in range(pasos):
    for i in range(pasos):      
        print(" ", end="")
    print("|")

for i in range(1):
    for i in range(pasos):
        print(" ", end="")
    print("V")

# Reto 4: Encapsula los comportamientos anteriores usando funciones
Usa funciones para dibujar la parte horizontal y vertical de la flecha.

pasos_adelante = 0
pasos_abajo = 0

pasos = input("Ingrese pasos hacia adelante: ")
pasos_adelante += int(pasos)

pasos_abajo = input("Ingrese pasos hacia abajo: ")
pasos_abajo = int(pasos_abajo)

def adelante():
    global pasos_adelante
    for i in range(pasos_adelante):
        print("-", end="")
    print(">")

def abajo():
    global pasos_abajo 
    for i in range(pasos_abajo):
        for i in range(pasos_adelante):
            print(" ", end="")      
        print("|")
    for i in range(1):
        for i in range(pasos_adelante):
            print(" ", end="")
        print("V")  

adelante()
abajo()

# Reto 5: La tortuga baja las escalas
Dibuja tres escalones que avanzan a la derecha y luego bajan.

pasos_adelante = 0
pasos_h = 0
pasos_v = 0

pasos_h = int(input("Ingrese pasos hacia adelante: "))
pasos_v = int(input("Ingrese pasos hacia abajo: "))

def adelante():
    global pasos_adelante, pasos_h
    print(" " * pasos_adelante , end="")
    print("-" * pasos_h + ">")
    pasos_adelante += pasos_h

def abajo():
    global pasos_adelante, pasos_v
    for i in range(pasos_v):
        print(" " * pasos_adelante + "|")
    print(" " * pasos_adelante + "v")

for i in range(3):
    adelante()
    abajo()


