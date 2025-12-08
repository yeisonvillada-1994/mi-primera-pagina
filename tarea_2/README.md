# Reto 1: Simular el comportamiento de la tortuga usando solo print() e input()
Este programa dibuja una flecha usando guiones y el símbolo >. 

from re import L

pasos = input("Ingrese pasos: ")
pasos = int(pasos)

for i in range(pasos):     
    print("-", end="")

print(">")



