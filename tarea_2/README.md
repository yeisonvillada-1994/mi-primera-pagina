# Reto 1: Simular el comportamiento de la tortuga usando solo print() e input()
Este fragmento de codigo pide cuántos pasos quieres avanzar y dibuja una flecha horizontal, cada paso se muestra como un guion - y al final se coloca el simbolo >.

```python
pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):     
    print("-", end="")

print(">")
```

# Reto 2: Tortuga bajando
Este fragmento de codigo pide cuántos pasos debe bajar la flecha, cada paso se representa con una línea vertical con el simbolo | y al final se dibuja la punta con el simbolo V.

```python
pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):
    print("|")

print("V")
```

# Reto 3: Girar y dibujar usando solo print() e input()
Este fragmento de codigo dibuja una flecha que primero va hacia la derecha y luego baja, primero imprime una línea horizontal de guiones, y después imprime líneas verticales alineadas para formar la parte de abajo.

```python
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
```

# Reto 4: Encapsula los comportamientos anteriores usando funciones
En este reto se crea una función que multiplica dos números.
La función recibe dos valores, los multiplica y devuelve el resultado.
Luego, el programa usa esa función enviándole dos números y muestra en pantalla la respuesta.

```python
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

```

# Reto 5: La tortuga baja las escalas
En este reto el programa pide al usuario que escriba dos números.
Después, una función toma esos dos valores, realiza la multiplicación y el programa muestra el resultado.

```python
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
```
### 📌 Nota
El código ejecutable está disponible en Google Colab para facilitar su prueba.
Link de Google Colab: https://colab.research.google.com/drive/1cw7IQs0W1Iu3MydBYI8ZfKa9jpmbs1-e#scrollTo=kUq8qZVun_wJ 
