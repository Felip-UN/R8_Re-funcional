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

## Perfiles:
### Stack overflow

[stack overflow](https://stackoverflow.com/users/29560901/felip-d1)

### linkedIn

[LinkedIn](https://www.linkedin.com/in/david-felipe-cortes-reyes-973201350/)

