# R8_Re-funcional
## Lambdas
**Nota rapida:** Ejercicios tomados del Reto 5

Se realizo en un solo programa, decidi usar ***x*** y ***y*** paralos argumentos porque anque se pudieran poner los mismos ***a*** y ***b*** quize copiar la segunda forma del ejemplo 3 (Funciones sin nombre - lambdas) en ***Funciones 2***
#### Programa
```python
from math import pi
a, b = map(int,input("Ingresa dos valores enteros separados por espacio: ").split())
print("Tus valores: ", a, b)
#cada lambda tiene argumentos x, y para probar si funcionan con cualquier variable mas adelante
# funciones anonimas con argumento y respectiva operacion:

#1
volumen_esfera= lambda x: (4/3)*pi*x**3 #Volumen de una esfera
v_es= volumen_esfera(a)
#2
volumen_cono= lambda x, y: pi*x**2*y/3 #Volumen de un cono
v_co= volumen_cono(a,b)
#3
area_figura= lambda x, y: x*y #Area de una figura, en este caso un rectangulo
a_fi=area_figura(a,b)

#Salidas, Probando un metodo para escribir cadenas
print((f"Una esfera de radio {a} tiene un volumen de {v_es}")) #segun busqué se llama f-string
print("Un cono de radio",a,"y altura",b,"tiene un volumen de",v_co) #Es mas eficiente que esto...
print(f"Un rectangulo de altura {a} y ancho {b} tiene un area de {a_fi}")
```
