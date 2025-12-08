# Reto 1: Simular el comportamiento de la tortuga usando solo print() e input()
Este programa dibuja una flecha usando guiones y el símbolo >.
# Reto1
# Este programa dibuja una flecha usando guiones y el símbolo ">"

from re import L

# Solicita al usuario que ingrese la cantidad de pasos
pasos = input("Ingrese pasos: ")

# Convierte el valor ingresado de texto a número entero
pasos = int(pasos)

# Ciclo que se ejecuta según la cantidad de pasos ingresados
for i in range(pasos):     
    # Imprime un guion sin salto de línea
    print("-", end="")

# Imprime el símbolo ">" al final de la flecha
print(">")


