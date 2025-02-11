# R8_Re-funcional
## Lambdas
**Nota rapida:** Ejercicios tomados del Reto 5

### Originales
```python
def volumen_esfera(r):
  voles = (4/3)*pi*r**3 #formula volumen de la esfera: V=(4/3)*pi*r**3
  return voles

def volumen_cono(r,h):
  volco=pi*r**2*h/3 # formula volumen del cono: pi*r**2*h/3
  return volco

def area_fig(b, h):
  area = b*h
  return area
```

### Lambdas
#### Programa
```python
#1
volumen_esfera= lambda x: (4/3)*pi*x**3 #Volumen de una esfera
v_es= volumen_esfera(a)

#2
volumen_cono= lambda x, y: pi*x**2*y/3 #Volumen de un cono
v_co= volumen_cono(a,b)

#3
area_figura= lambda x, y: x*y #Area de una figura, en este caso un rectangulo
a_fi=area_figura(a,b)

```

## Ejecucion
```python
import time 
from math import pi
a, b=map(int, input("Ingresa dos valores enteros separados por espacio: ").split())
start_time = time.time()
print("Tus valores: ", a, b)
#cada lambda tiene argumentos x, y para probar si funcionan con cualquier variable mas adelante

# funciones anonimas con argumento y respectiva operacion:
volumen_esfera= lambda x: (4/3)*pi*x**3 #Volumen de una esfera
v_es= volumen_esfera(a)

volumen_cono= lambda x, y: pi*x**2*y/3 #Volumen de un cono
v_co= volumen_cono(a,b)

area_figura= lambda x, y: x*y #Area de una figura, en este caso un rectangulo
a_fi=area_figura(a,b)

print((f"Una esfera de radio {a} tiene un volumen de {v_es}")) #los visto en clase de cadenas :)
print(f"Un cono de radio",{a},"y altura",{b},"tiene un volumen de",v_co)
print(f"Un rectangulo de altura {a} y ancho {b} tiene un area de {a_fi}")
end_time = time.time()

timer = end_time - start_time
print("timer: ",timer)
```
**Salida consola:**

```python
Ingresa dos valores enteros separados por espacio: 4 5
Tus valores:  4 5
Una esfera de radio 4 tiene un volumen de 268.082573106329
Un cono de radio {4} y altura {5} tiene un volumen de 83.77580409572782
Un rectangulo de altura 4 y ancho 5 tiene un area de 20
timer:  0.005732297897338867
```
## *args



### arg 1
El punto esta en el circulo?
```python
import time

start_time = time.time()

def punto_en_c(*args)-> int:
  circulo=(0,0,5)
  d_cuadrada=((args[0] - circulo[0])**2 + (args[1] - circulo[1])**2)
  if d_cuadrada<circulo[2]**2:
    return ("Tu punto marcado se encuentra dentro del circulo")
  elif d_cuadrada==circulo[2]**2:
    return ("Tu punto está sobre el borde del círculo")
  else:
    return ("Tu punto marcado esta fuera del circulo")

x1=1
y1=3
print(f"Punto 1: {x1},{y1}")
salida=punto_en_c(x1,y1)
print(salida)
x2=5
y2=6
print(f"Punto 2: {x2},{y2}")
salida1=punto_en_c(x2, y2)
print(salida1)
end_time = time.time()

timer = end_time - start_time
print("timer: ",timer)
```
**Salida de consola:**
```python
Punto 1: 1,3
Tu punto marcado se encuentra dentro del circulo
Punto 2: 5,6
Tu punto marcado esta fuera del circulo
timer:  0.0010387897491455078
```

### arg 2
Tabla de un numero fijo por 4 valores diferentes (o iguales si lo deseas :/)  tuve una idea mas clara al ver esta pagina: [Uso de *args y **kwargs](https://python-intermedio.readthedocs.io/es/latest/args_and_kwargs.html)
```python
import time
def tabla_de(fijo, *multiple):
  for num in multiple:
    print(f"{fijo} x {num} = {fijo*num}")

if __name__=="__main__":
  num=int(input("Que numero quieres probar?: "))
  print("probemos con cuatro numeros:")
  n=input("ingresa 4 numeros separados por 1 espacio: ")
  start_time = time.time()
  numeros=list(map(int, n.split(" "))) #transformar la cadena "n" en una lista de 4 valores
  n1=numeros[0]
  n2=numeros[1]
  n3=numeros[2]
  n4=numeros[3]
  tabla=tabla_de(num, n1, n2, n3, n4)
  print(tabla)

  end_time = time.time()

  timer = end_time - start_time
  print("timer: ",timer)
```
**Salida de consola:**
```python
Que numero quieres probar?: 5
probemos con cuatro numeros:
ingresa 4 numeros separados por 1 espacio: 3 4 5 6
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
None
timer:  0.0002117156982421875
```
Nota: no se porque salio el "None" XD

## Recursiva (WHY?!)
En este caso este fue el mas complicado, aun sigo confundido frente al uso de estas pero aqui hay un programa que hcae el trabajo :/
```python
def potencia(base, exponente):
  if exponente == 0:# cualquier número elevado a 0 es 1
      return 1
  
  else:
      return base * potencia(base, exponente - 1) #Caso recursivo: a^b = a * a^(b-1)

resultado = potencia(2, 3)
print(resultado)  # Debería imprimir 8 (2^3)

```
**Salida de consola:**
8

## Enlaces Perfiles:
### Stack overflow
![stack_check](https://github.com/user-attachments/assets/e4f2f06f-f502-413f-83ce-cb2619cc6111)

[stack overflow](https://stackoverflow.com/users/29560901/felip-d1)

### linkedIn

[LinkedIn](https://www.linkedin.com/in/david-felipe-cortes-reyes-973201350/)

