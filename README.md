# Trabajo-extra-Programacion
Archivo con ejercicios resueltos del libro de Joyanes
# TRABAJO DE PUNTOS EXTRAS

**Resolver: libro de Joyanes **

* Arreglos: Unidomensionales y bidimensionales *
-------------
## *EJERCICIOS PROPUESTOS*

**EJERCICIO 7.1**

```python
I = 1
J = 2
A = [0] * 11  # índice 1 a 10

A[I] = J
A[J] = I
A[J+1] = I + J
I = A[I] + A[J]
A[3] = 5
J = A[I] - A[J]

print("I =", I)
print("J =", J)
```

```
    Proceso Ejercicio7_1
    Definir I, J Como Entero
    Dimension A[10]

    I <- 1
    J <- 2

    A[I] <- J
    A[J] <- I
    A[J+1] <- I + J
    I <- A[I] + A[J]
    A[3] <- 5
    J <- A[I] - A[J]

    Escribir "I = ", I
    Escribir "J = ", J
    FinProceso
```

**EJERCICIO 7.2**

Contar elementos positivos de un vector

```python
n = int(input("Ingrese cantidad de elementos: "))
vector = []
contador = 0

for i in range(n):
    num = float(input("Ingrese número: "))
    vector.append(num)
    if num > 0:
        contador += 1

print("Cantidad de positivos:", contador)
```

```
    Proceso Ejercicio7_2
      Definir n, i, contador Como Entero
      Definir num Como Real
      Dimension vector[100]

      contador <- 0
      Escribir "Ingrese cantidad de elementos:"
      Leer n

      Para i <- 1 Hasta n Hacer
          Escribir "Ingrese número:"
          Leer num
          vector[i] <- num

         Si num > 0 Entonces
              contador <- contador + 1
          FinSi
    FinPara

    Escribir "Cantidad de positivos:", contador
  FinProceso
```

**EJERCICIO 7.3**

Matriz identidad 4x4
```python
n = 4
matriz = []

for i in range(n):
    fila = []
    for j in range(n):
        if i == j:
            fila.append(1)
        else:
            fila.append(0)
    matriz.append(fila)

for fila in matriz:
    print(fila)
```

```
    Proceso Ejercicio7_3
      Definir i, j Como Entero
      Dimension matriz[4,4]

      Para i <- 1 Hasta 4 Hacer
        Para j <- 1 Hasta 4 Hacer
            Si i = j Entonces
                matriz[i,j] <- 1
            SiNo
                matriz[i,j] <- 0
            FinSi
        FinPara
      FinPara

      Para i <- 1 Hasta 4 Hacer
        Para j <- 1 Hasta 4 Hacer
            Escribir matriz[i,j], " " Sin Saltar
        FinPara
        Escribir ""
      FinPara
    FinProceso
```

**EJERCICIO 7.4**

Suma de filas y columnas (matriz 3x3)
```python
matriz = []
for i in range(3):
    fila = []
    for j in range(3):
        num = float(input(f"Ingrese elemento [{i}][{j}]: "))
        fila.append(num)
    matriz.append(fila)

suma_filas = [0]*3
suma_columnas = [0]*3

for i in range(3):
    for j in range(3):
        suma_filas[i] += matriz[i][j]
        suma_columnas[j] += matriz[i][j]

print("Suma de filas:", suma_filas)
print("Suma de columnas:", suma_columnas)
```

```
    Proceso Ejercicio7_4
      Definir i, j Como Entero
      Dimension matriz[3,3]
      Dimension sumaFilas[3]
      Dimension sumaColumnas[3]

      Para i <- 1 Hasta 3 Hacer
        sumaFilas[i] <- 0
        sumaColumnas[i] <- 0
      FinPara

      Para i <- 1 Hasta 3 Hacer
        Para j <- 1 Hasta 3 Hacer
            Escribir "Ingrese elemento:", i, j
            Leer matriz[i,j]
            sumaFilas[i] <- sumaFilas[i] + matriz[i,j]
            sumaColumnas[j] <- sumaColumnas[j] + matriz[i,j]
          FinPara
      FinPara

      Escribir "Suma filas:"
      Para i <- 1 Hasta 3 Hacer
        Escribir sumaFilas[i]
      FinPara

      Escribir "Suma columnas:"
      Para i <- 1 Hasta 3 Hacer
        Escribir sumaColumnas[i]
      FinPara
    FinProceso
```

**EJERCICIO 7.5**

Suma total y media de un vector
```python
n = int(input("Cantidad de elementos: "))
vector = []
suma = 0

for i in range(n):
    num = float(input("Ingrese número: "))
    vector.append(num)
    suma += num

media = suma / n

print("Suma total:", suma)
print("Media:", media)
```

```
    Proceso Ejercicio7_5
      Definir n, i Como Entero
      Definir suma, num, media Como Real
      Dimension vector[100]

      suma <- 0
      Escribir "Cantidad de elementos:"
      Leer n

      Para i <- 1 Hasta n Hacer
        Escribir "Ingrese número:"
        Leer num
        vector[i] <- num
        suma <- suma + num
      FinPara

      media <- suma / n

      Escribir "Suma total:", suma
      Escribir "Media:", media
    FinProceso
```

**EJERCICIO 7.6**

Calcular número de negativos, ceros y positivos de un vector de 60 elementos.
```python
positivos = 0
negativos = 0
ceros = 0

for i in range(60):
    num = float(input(f"Ingrese número {i+1}: "))
    
    if num > 0:
        positivos += 1
    elif num < 0:
        negativos += 1
    else:
        ceros += 1

print("Positivos:", positivos)
print("Negativos:", negativos)
print("Ceros:", ceros)
```

```
    Proceso Ejercicio7_6
      Definir i, positivos, negativos, ceros Como Entero
      Definir num Como Real

      positivos <- 0
      negativos <- 0
      ceros <- 0

      Para i <- 1 Hasta 60 Hacer
        Escribir "Ingrese número:"
        Leer num
        
        Si num > 0 Entonces
            positivos <- positivos + 1
        SiNo
            Si num < 0 Entonces
                negativos <- negativos + 1
            SiNo
                ceros <- ceros + 1
            FinSi
        FinSi
      FinPara

      Escribir "Positivos:", positivos
      Escribir "Negativos:", negativos
      Escribir "Ceros:", ceros
    FinProceso
```
**EJERCICIO 7.7**

Suma de la diagonal principal de una matriz 4x4
```python
matriz = []
suma = 0

for i in range(4):
    fila = []
    for j in range(4):
        num = float(input(f"Ingrese elemento [{i}][{j}]: "))
        fila.append(num)
    matriz.append(fila)

for i in range(4):
    suma += matriz[i][i]

print("Suma diagonal principal:", suma)
```

```
    Proceso Ejercicio7_7
      Definir i, j Como Entero
      Definir suma Como Real
      Dimension matriz[4,4]

      suma <- 0

      Para i <- 1 Hasta 4 Hacer
        Para j <- 1 Hasta 4 Hacer
            Escribir "Ingrese elemento:", i, j
            Leer matriz[i,j]
        FinPara
      FinPara

      Para i <- 1 Hasta 4 Hacer
        suma <- suma + matriz[i,i]
      FinPara

      Escribir "Suma diagonal principal:", suma
    FinProceso
```
**EJERCICIO 7.8**

Dividir todos los elementos del vector T entre T[K]
```python
T = []
for i in range(50):
    num = float(input(f"Ingrese número {i+1}: "))
    T.append(num)

K = int(input("Ingrese posición K (1-50): ")) - 1

if T[K] != 0:
    nueva_tabla = []
    for i in range(50):
        nueva_tabla.append(T[i] / T[K])
    
    print("Nueva tabla:")
    print(nueva_tabla)
else:
    print("No se puede dividir por cero.")
```

```
    Proceso Ejercicio7_8
      Definir i, K Como Entero
      Dimension T[50]
      Dimension nueva[50]

      Para i <- 1 Hasta 50 Hacer
        Escribir "Ingrese número:"
        Leer T[i]
      FinPara

      Escribir "Ingrese posición K (1-50):"
      Leer K

      Si T[K] <> 0 Entonces
        Para i <- 1 Hasta 50 Hacer
            nueva[i] <- T[i] / T[K]
        FinPara
        
        Escribir "Nueva tabla:"
        Para i <- 1 Hasta 50 Hacer
            Escribir nueva[i]
        FinPara
      SiNo
        Escribir "No se puede dividir por cero"
      FinSi
    FinProceso
```
**EJERCICIO 7.9

Insertar valor X en posición k de un vector
```python
N = int(input("Cantidad de elementos actuales: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

X = float(input("Valor a insertar: "))
k = int(input("Posición donde insertar (1 a N+1): ")) - 1

vector.insert(k, X)

print("Vector actualizado:")
print(vector)
```

```
    Proceso Ejercicio7_9
      Definir N, i, k Como Entero
      Definir X Como Real
      Dimension vector[100]

      Escribir "Cantidad de elementos:"
      Leer N

      Para i <- 1 Hasta N Hacer
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara

      Escribir "Valor a insertar:"
      Leer X

      Escribir "Posición donde insertar:"
      Leer k

      Para i <- N Hasta k Con Paso -1 Hacer
        vector[i+1] <- vector[i]
      FinPara

      vector[k] <- X
      N <- N + 1

      Escribir "Vector actualizado:"
      Para i <- 1 Hasta N Hacer
        Escribir vector[i]
      FinPara
    FinProceso
```

**EJERCICIO 7.10**

Sistema de reservas avión (300 plazas)

```python
# Ejercicio 7.10

plazas = [0] * 301  # 1 a 300

while True:
    print("\n1. Reservar")
    print("2. Cancelar")
    print("3. Salir")
    opcion = int(input("Opción: "))
    
    if opcion == 1:
        asiento = int(input("Número de asiento (1-300): "))
        
        if plazas[asiento] == 0:
            plazas[asiento] = 1
            print("Reserva realizada.")
        else:
            print("Asiento ocupado.")
    
    elif opcion == 2:
        asiento = int(input("Número de asiento a cancelar: "))
        plazas[asiento] = 0
        print("Reserva cancelada.")
    
    elif opcion == 3:
        print("Cerrando sistema...")
        break

```

```
    Proceso Ejercicio7_10
      Definir plazas Como Entero
      Definir opcion, asiento Como Entero
      Dimension plazas[300]
    
      Para asiento <- 1 Hasta 300 Hacer
        plazas[asiento] <- 0
      FinPara
    
      Repetir
        Escribir "1. Reservar"
        Escribir "2. Cancelar"
        Escribir "3. Salir"
        Leer opcion
        
        Si opcion = 1 Entonces
            Escribir "Número de asiento (1-300):"
            Leer asiento
            
            Si plazas[asiento] = 0 Entonces
                plazas[asiento] <- 1
                Escribir "Reserva realizada"
            SiNo
                Escribir "Asiento ocupado"
            FinSi
        FinSi
        
        Si opcion = 2 Entonces
            Escribir "Número de asiento a cancelar:"
            Leer asiento
            plazas[asiento] <- 0
            Escribir "Reserva cancelada"
        FinSi
        
      Hasta Que opcion = 3
    
      Escribir "Sistema cerrado"
    FinProceso
```
**EJERCICIO 7.11**

Calcular la media de cada alumno (8 asignaturas con coeficientes) y luego:

Media general de la clase

Media por asignatura

Porcentaje de faltas
```python
# 7.11 - Medias de alumnos

num_alumnos = int(input("Ingrese número de alumnos: "))
num_asignaturas = 8

notas = []
coeficientes = []

print("Ingrese los coeficientes de las 8 asignaturas:")
for i in range(num_asignaturas):
    coef = float(input(f"Coeficiente asignatura {i+1}: "))
    coeficientes.append(coef)

for i in range(num_alumnos):
    print(f"\nAlumno {i+1}")
    notas_alumno = []
    for j in range(num_asignaturas):
        nota = float(input(f"Nota asignatura {j+1}: "))
        notas_alumno.append(nota)
    notas.append(notas_alumno)

# Media por alumno
medias_alumnos = []
for i in range(num_alumnos):
    suma = 0
    suma_coef = 0
    for j in range(num_asignaturas):
        suma += notas[i][j] * coeficientes[j]
        suma_coef += coeficientes[j]
    media = suma / suma_coef
    medias_alumnos.append(media)
    print(f"Media alumno {i+1}: {media}")

# Media general
media_general = sum(medias_alumnos) / num_alumnos
print("Media general de la clase:", media_general)
```

```
    Proceso MediasClase
      Definir num_alumnos, num_asignaturas Como Entero
      num_asignaturas <- 8
    
      Escribir "Ingrese número de alumnos:"
      Leer num_alumnos
    
      Dimension coeficientes[8]
      Dimension notas[num_alumnos,8]
    
      Para i <- 1 Hasta 8
        Escribir "Coeficiente asignatura ", i
        Leer coeficientes[i]
      FinPara
    
      Para i <- 1 Hasta num_alumnos
        Para j <- 1 Hasta 8
            Escribir "Nota alumno ", i, " asignatura ", j
            Leer notas[i,j]
        FinPara
      FinPara
    
      Para i <- 1 Hasta num_alumnos
        suma <- 0
        suma_coef <- 0
        Para j <- 1 Hasta 8
            suma <- suma + notas[i,j] * coeficientes[j]
            suma_coef <- suma_coef + coeficientes[j]
        FinPara
        media <- suma / suma_coef
        Escribir "Media alumno ", i, ": ", media
      FinPara
    FinProceso
```
**EJERCICIO 7.12**

Cuadrado de los 100 primeros números
```python
cuadrados = []

for i in range(1, 101):
    cuadrados.append(i**2)

print(cuadrados)
```

```
    Proceso Cuadrados
      Dimension tabla[100]
    
      Para i <- 1 Hasta 100
        tabla[i] <- i * i
      FinPara
    
      Para i <- 1 Hasta 100
        Escribir tabla[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.13**

Dadas N temperaturas, calcular:

La media

Cuántas son mayores o iguales a la media
```python
# Ejercicio 7.13

N = int(input("Cantidad de temperaturas: "))
temperaturas = []
suma = 0

for i in range(N):
    temp = float(input(f"Temperatura {i+1}: "))
    temperaturas.append(temp)
    suma += temp

media = suma / N
contador = 0

for temp in temperaturas:
    if temp >= media:
        contador += 1

print("Media:", media)
print("Temperaturas mayores o iguales a la media:", contador)
```

```
    Proceso Ejercicio7_13
      Definir N, i, contador Como Entero
      Definir temp, suma, media Como Real
      Dimension temperaturas[100]
    
      suma <- 0
      contador <- 0
    
      Escribir "Cantidad de temperaturas:"
      Leer N
    
      Para i <- 1 Hasta N
        Escribir "Temperatura:"
        Leer temp
        temperaturas[i] <- temp
        suma <- suma + temp
      FinPara
    
      media <- suma / N
    
      Para i <- 1 Hasta N
        Si temperaturas[i] >= media Entonces
            contador <- contador + 1
        FinSi
      FinPara
    
      Escribir "Media:", media
      Escribir "Mayores o iguales a la media:", contador
    FinProceso
```

**EJERCICIO 7.14**

Calcular suma y media de un vector de 100 elementos
```python

suma = 0

for i in range(100):
    num = float(input(f"Número {i+1}: "))
    suma += num

media = suma / 100

print("Suma:", suma)
print("Media:", media)
```

```
    Proceso Ejercicio7_14
      Definir i Como Entero
      Definir num, suma, media Como Real
    
      suma <- 0
    
      Para i <- 1 Hasta 100
        Escribir "Número:"
        Leer num
        suma <- suma + num
      FinPara
    
      media <- suma / 100
    
      Escribir "Suma:", suma
      Escribir "Media:", media
    FinProceso
```
**EJERCICIO 7.15**

Calcular el mayor valor de una lista de N elementos

```python
N = int(input("Cantidad de elementos: "))
mayor = float(input("Ingrese número 1: "))

for i in range(2, N+1):
    num = float(input(f"Ingrese número {i}: "))
    if num > mayor:
        mayor = num

print("El mayor valor es:", mayor)
```

```
    Proceso Ejercicio7_15
      Definir N, i Como Entero
      Definir num, mayor Como Real
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Escribir "Ingrese número 1:"
      Leer mayor
    
      Para i <- 2 Hasta N
        Escribir "Ingrese número:"
        Leer num
        Si num > mayor Entonces
            mayor <- num
        FinSi
      FinPara
    
      Escribir "El mayor valor es:", mayor
    FinProceso
```
**EJERCICIO 7.16**

Calcular:

Suma de números pares

Suma de números impares
```python

N = int(input("Cantidad de elementos: "))
suma_pares = 0
suma_impares = 0

for i in range(N):
    num = int(input("Ingrese número entero: "))
    
    if num % 2 == 0:
        suma_pares += num
    else:
        suma_impares += num

print("Suma pares:", suma_pares)
print("Suma impares:", suma_impares)
```

```
    Proceso Ejercicio7_16
      Definir N, i, num Como Entero
      Definir suma_pares, suma_impares Como Entero
    
      suma_pares <- 0
      suma_impares <- 0
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N
        Escribir "Ingrese número entero:"
        Leer num
        
        Si num MOD 2 = 0 Entonces
            suma_pares <- suma_pares + num
        SiNo
            suma_impares <- suma_impares + num
        FinSi
      FinPara
    
      Escribir "Suma pares:", suma_pares
      Escribir "Suma impares:", suma_impares
    FinProceso
```

**EJERCICIO 7.17**

Invertir los elementos de un vector
```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

vector_invertido = vector[::-1]

print("Vector invertido:")
print(vector_invertido)
```

```
    Proceso Ejercicio7_17
      Definir N, i Como Entero
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara
    
      Escribir "Vector invertido:"
      Para i <- N Hasta 1 Con Paso -1
        Escribir vector[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.18**

Contar cuántas veces aparece un número X en el vector
```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

X = float(input("Número a buscar: "))
contador = vector.count(X)

print("El número aparece", contador, "veces.")
```

```
    Proceso Ejercicio7_18
      Definir N, i, contador Como Entero
      Definir X Como Real
      Dimension vector[100]
    
      contador <- 0
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara
    
      Escribir "Número a buscar:"
      Leer X
    
      Para i <- 1 Hasta N
        Si vector[i] = X Entonces
            contador <- contador + 1
        FinSi
      FinPara
    
      Escribir "El número aparece ", contador, " veces."
    FinProceso
```
**EJERCICIO 7.19**

Eliminar un elemento en posición K
```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

K = int(input("Posición a eliminar (1 a N): ")) - 1

if 0 <= K < N:
    vector.pop(K)
    print("Vector actualizado:")
    print(vector)
else:
    print("Posición inválida.")
```

```
    Proceso Ejercicio7_19
      Definir N, i, K Como Entero
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N Hacer
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara
    
      Escribir "Posición a eliminar:"
      Leer K
    
      Para i <- K Hasta N-1
        vector[i] <- vector[i+1]
      FinPara
    
      N <- N - 1
    
      Escribir "Vector actualizado:"
      Para i <- 1 Hasta N
        Escribir vector[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.20**

Ordenar un vector (método burbuja)
```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

# Método burbuja
for i in range(N):
    for j in range(0, N - i - 1):
        if vector[j] > vector[j + 1]:
            vector[j], vector[j + 1] = vector[j + 1], vector[j]

print("Vector ordenado:")
print(vector)
```

```
    Proceso Ejercicio7_20
      Definir N, i, j Como Entero
      Definir aux Como Real
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N Hacer
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara
    
      Para i <- 1 Hasta N-1
        Para j <- 1 Hasta N-i
            Si vector[j] > vector[j+1] Entonces
                aux <- vector[j]
                vector[j] <- vector[j+1]
                vector[j+1] <- aux
            FinSi
        FinPara
      FinPara
    
      Escribir "Vector ordenado:"
      Para i <- 1 Hasta N
        Escribir vector[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.21**

Buscar un número en el vector y mostrar su posición
```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

X = float(input("Número a buscar: "))

if X in vector:
    posicion = vector.index(X) + 1
    print("Número encontrado en posición:", posicion)
else:
    print("Número no encontrado.")
```

```
    Proceso Ejercicio7_21
      Definir N, i, posicion Como Entero
      Definir X Como Real
      Dimension vector[100]
    
      posicion <- 0
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N Hacer
        Escribir "Ingrese número:"
        Leer vector[i]
      FinPara
    
      Escribir "Número a buscar:"
      Leer X
    
      Para i <- 1 Hasta N
        Si vector[i] = X Entonces
            posicion <- i
        FinSi
      FinPara
    
      Si posicion > 0 Entonces
        Escribir "Número encontrado en posición:", posicion
      SiNo
        Escribir "Número no encontrado."
      FinSi
    FinProceso
```
**EJERCICIO 7.22**

Copiar un vector en otro
```python
N = int(input("Cantidad de elementos: "))
vector1 = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector1.append(num)

vector2 = vector1.copy()

print("Vector copiado:")
print(vector2)
```

```
    Proceso Ejercicio7_22
      Definir N, i Como Entero
      Dimension vector1[100], vector2[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N Hacer
        Escribir "Ingrese número:"
        Leer vector1[i]
        vector2[i] <- vector1[i]
      FinPara
    
      Escribir "Vector copiado:"
      Para i <- 1 Hasta N
        Escribir vector2[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.23**

Sumar dos vectores y guardar en un tercero
```python
N = int(input("Cantidad de elementos: "))
A = []
B = []
C = []

print("Vector A")
for i in range(N):
    A.append(float(input("Ingrese número: ")))

print("Vector B")
for i in range(N):
    B.append(float(input("Ingrese número: ")))

for i in range(N):
    C.append(A[i] + B[i])

print("Vector suma:")
print(C)
```

```
    Proceso Ejercicio7_23
      Definir N, i Como Entero
      Dimension A[100], B[100], C[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Escribir "Vector A"
      Para i <- 1 Hasta N
        Leer A[i]
      FinPara
    
      Escribir "Vector B"
      Para i <- 1 Hasta N
        Leer B[i]
      FinPara
    
      Para i <- 1 Hasta N
        C[i] <- A[i] + B[i]
      FinPara
    
      Escribir "Vector suma:"
      Para i <- 1 Hasta N
        Escribir C[i]
      FinPara
    FinProceso
```

**EJERCICIO 7.24**

Intercambiar dos posiciones del vector
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

i1 = int(input("Primera posición: ")) - 1
i2 = int(input("Segunda posición: ")) - 1

vector[i1], vector[i2] = vector[i2], vector[i1]

print("Vector actualizado:")
print(vector)
```

```
    Proceso Ejercicio7_24
      Definir N, i, i1, i2 Como Entero
      Definir aux Como Real
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N
        Leer vector[i]
      FinPara
    
      Escribir "Primera posición:"
      Leer i1
      Escribir "Segunda posición:"
      Leer i2
    
      aux <- vector[i1]
      vector[i1] <- vector[i2]
      vector[i2] <- aux
    
      Escribir "Vector actualizado:"
      Para i <- 1 Hasta N
        Escribir vector[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.25**

Contar positivos, negativos y ceros
```python
N = int(input("Cantidad de elementos: "))
positivos = negativos = ceros = 0

for i in range(N):
    num = float(input("Ingrese número: "))
    
    if num > 0:
        positivos += 1
    elif num < 0:
        negativos += 1
    else:
        ceros += 1

print("Positivos:", positivos)
print("Negativos:", negativos)
print("Ceros:", ceros)
```

```
    Proceso Ejercicio7_25
      Definir N, i Como Entero
      Definir num Como Real
      Definir positivos, negativos, ceros Como Entero
    
      positivos <- 0
      negativos <- 0
      ceros <- 0
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N
        Leer num
        
        Si num > 0 Entonces
            positivos <- positivos + 1
        Sino
            Si num < 0 Entonces
                negativos <- negativos + 1
            Sino
                ceros <- ceros + 1
            FinSi
        FinSi
      FinPara
    
      Escribir "Positivos:", positivos
      Escribir "Negativos:", negativos
      Escribir "Ceros:", ceros
    FinProceso
```
**EJERCICIO 7.26**

Unir dos vectores en uno solo
```python
N = int(input("Cantidad de elementos del vector A: "))
M = int(input("Cantidad de elementos del vector B: "))

A = []
B = []

print("Vector A")
for i in range(N):
    A.append(float(input("Ingrese número: ")))

print("Vector B")
for i in range(M):
    B.append(float(input("Ingrese número: ")))

C = A + B

print("Vector unido:")
print(C)
```

```
    Proceso Ejercicio7_26
      Definir N, M, i Como Entero
      Dimension A[100], B[100], C[200]
    
      Escribir "Cantidad elementos A:"
      Leer N
    
      Para i <- 1 Hasta N
        Leer A[i]
      FinPara
    
      Escribir "Cantidad elementos B:"
      Leer M
    
      Para i <- 1 Hasta M
        Leer B[i]
        C[N+i] <- B[i]
      FinPara
    
      Para i <- 1 Hasta N
        C[i] <- A[i]
      FinPara
    
      Escribir "Vector unido:"
      Para i <- 1 Hasta N+M
        Escribir C[i]
      FinPara
    FinProceso
```
**EJERCICIO 7.27**

Eliminar valores repetidos
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

sin_repetidos = list(set(vector))

print("Vector sin repetidos:")
print(sin_repetidos)
```

```
    Proceso Ejercicio7_27
      Definir N, i, j Como Entero
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Para i <- 1 Hasta N Hacer
        Leer vector[i]
      FinPara
    
      Para i <- 1 Hasta N
        Para j <- i+1 Hasta N
            Si vector[i] = vector[j] Entonces
                vector[j] <- -99999
            FinSi
        FinPara
      FinPara
    
      Escribir "Vector sin repetidos:"
      Para i <- 1 Hasta N
        Si vector[i] <> -99999 Entonces
            Escribir vector[i]
        FinSi
      FinPara
    FinProceso
```
**EJERCICIO 7.28**

Buscar el menor valor del vector
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

menor = min(vector)

print("El menor valor es:", menor)
```

```
    Proceso Ejercicio7_28
      Definir N, i Como Entero
      Definir menor Como Real
      Dimension vector[100]
    
      Escribir "Cantidad de elementos:"
      Leer N
    
      Escribir "Ingrese número:"
      Leer menor
    
      vector[1] <- menor
    
      Para i <- 2 Hasta N
        Leer vector[i]
        Si vector[i] < menor Entonces
            menor <- vector[i]
        FinSi
      FinPara
    
      Escribir "El menor valor es:", menor
    FinProceso
```

# EJERCICIOS RESUELTOS(Arreglos)
**Ejercicio 7.1**

Escribir un algoritmo que permita calcular el cuadrado de los cien primeros números enteros y a continuación es cribir una tabla que contenga dichos cien números cuadrados.

```
Algoritmo cuadrados
	Definir tabla Como Entero
	Dimension tabla[101]
	Definir i, c Como Entero

	Escribir "Numero", "    ", "Cuadrado"
	Escribir "--------------------"

	Para i <- 1 Hasta 100 Hacer
		c <- i * i
		tabla[i] <- c
		Escribir i, "        ", tabla[i]
	FinPara
FinAlgoritmo

```
```python
tabla = [0] * 100   # arreglo (lista) de 100 posiciones

print("Numero    Cuadrado")
print("--------------------")

for i in range(1, 101):
    tabla[i - 1] = i * i
    print(i, "       ", tabla[i - 1])

```
**Ejercicio 7.2**

Se tienen N temperaturas. Se desea calcular su media y determinar entre todas ellas cuáles son superiores o iguales a esa media.

```
Algoritmo Temperaturas
    Definir N, I, C Como Entero
    Definir suma, media Como Real

    Escribir "Ingrese la cantidad de temperaturas:"
    Leer N

    Dimension Temp[N]

    suma <- 0
    C <- 0

    Para I <- 0 Hasta N-1 Hacer
        Escribir "Ingrese la temperatura ", I+1, ":"
        Leer Temp[I]
        suma <- suma + Temp[I]
    FinPara

    media <- suma / N

    Escribir "Temperaturas mayores o iguales a la media:"
    Para I <- 0 Hasta N-1 Hacer
        Si Temp[I] >= media Entonces
            Escribir Temp[I]
            C <- C + 1
        FinSi
    FinPara

    Escribir "La media es: ", media
    Escribir "Cantidad de temperaturas mayores o iguales a la media: ", C
FinAlgoritmo
```
```python
N = int(input("Ingrese la cantidad de temperaturas: "))

Temp = []  # arreglo (lista) de temperaturas
suma = 0
C = 0

for i in range(N):
    t = float(input(f"Ingrese la temperatura {i + 1}: "))
    Temp.append(t)
    suma += t

media = suma / N

print("Temperaturas mayores o iguales a la media:")
for i in range(N):
    if Temp[i] >= media:
        print(Temp[i])
        C += 1

print("La media es:", media)
print("Cantidad de temperaturas mayores o iguales a la media:", C)

```
**Ejercicio 7.3**

Escribir el algoritmo que permita sumar el número de elementos positivos y el de negativos de una tabla T
```
Proceso ActividadResuelta3;

    Definir N, i, posicion Como Entero;
    Definir buscado Como Real;
    Dimension vector[100];

    posicion <- 0;

    Escribir "Cantidad de elementos:";
    Leer N;

    Para i <- 1 Hasta N Hacer
        Leer vector[i];
    FinPara

    Escribir "Número a buscar:";
    Leer buscado;

    Para i <- 1 Hasta N Hacer
        Si vector[i] = buscado Entonces
            posicion <- i;
        FinSi
    FinPara

    Si posicion <> 0 Entonces
        Escribir "Número encontrado en posición: ", posicion;
    SiNo
        Escribir "Número no encontrado.";
    FinSi

FinProceso

```

```python

N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    num = float(input("Ingrese número: "))
    vector.append(num)

buscado = float(input("Número a buscar: "))
encontrado = False

for i in range(N):
    if vector[i] == buscado:
        print("Número encontrado en posición:", i + 1)
        encontrado = True
        break

if not encontrado:
    print("Número no encontrado.")

```

****Ejercicio 7.4**
Inicializar una matriz de dos dimensiones con un valor constante dado K.
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

for i in range(N - 1):
    for j in range(N - i - 1):
        if vector[j] > vector[j + 1]:
            vector[j], vector[j + 1] = vector[j + 1], vector[j]

print("Vector ordenado:")
print(vector)

```
```
Proceso ActividadResuelta4;

    Definir N, i, j Como Entero;
    Definir aux Como Real;
    Dimension vector[100];

    Escribir "Cantidad de elementos:";
    Leer N;

    Para i <- 1 Hasta N Hacer
        Leer vector[i];
    FinPara

    Para i <- 1 Hasta N-1 Hacer
        Para j <- 1 Hasta N-i Hacer
            Si vector[j] > vector[j+1] Entonces
                aux <- vector[j];
                vector[j] <- vector[j+1];
                vector[j+1] <- aux;
            FinSi
        FinPara
    FinPara

    Escribir "Vector ordenado:";
    Para i <- 1 Hasta N Hacer
        Escribir vector[i];
    FinPara

FinProceso


```
**Ejercicio 7.5**
Realizar la suma de dos matrices bidimensionales.
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

pos = int(input("Posición donde insertar: ")) - 1
valor = float(input("Valor a insertar: "))

vector.insert(pos, valor)

print("Vector actualizado:")
print(vector)

```

```
Proceso ActividadResuelta5

    Definir N, i, pos Como Entero;
    Definir valor Como Real;
    Dimension vector[101];

    Escribir "Cantidad de elementos:";
    Leer N;

    Para i <- 1 Hasta N Hacer
        Leer vector[i];
    FinPara

    Escribir "Posición donde insertar:";
    Leer pos;

    Escribir "Valor a insertar:";
    Leer valor;

    Para i <- N Hasta pos Con Paso -1 Hacer
        vector[i+1] <- vector[i];
    FinPara

    vector[pos] <- valor;
    N <- N + 1;

    Escribir "Vector actualizado:";
    Para i <- 1 Hasta N Hacer
        Escribir vector[i];
    FinPara

FinProceso


```

**Ejercicio 7.6**
Se dispone de una tabla T de dos dimensiones. Calcular la suma de sus elementos.
```python
N = int(input("Cantidad de elementos: "))
vector = []

for i in range(N):
    vector.append(float(input("Ingrese número: ")))

pos = int(input("Posición a eliminar: ")) - 1

if 0 <= pos < N:
    vector.pop(pos)
    print("Vector actualizado:")
    print(vector)
else:
    print("Posición inválida.")

```

```
Proceso ActividadResuelta6

    Definir N, i, pos Como Entero;
    Dimension vector[100];

    Escribir "Cantidad de elementos:";
    Leer N;

    Para i <- 1 Hasta N Hacer
        Leer vector[i];
    FinPara

    Escribir "Posición a eliminar:";
    Leer pos;

    Para i <- pos Hasta N-1 Hacer
        vector[i] <- vector[i+1];
    FinPara

    N <- N - 1;

    Escribir "Vector actualizado:";
    Para i <- 1 Hasta N Hacer
        Escribir vector[i];
    FinPara

FinProceso

```

**Ejercicio 7.7**
Realizar la búsqueda de un determinado nombre en una lista de nombres, de modo que el algoritmo imprima los
siguientes mensajes según el resultado:
```python
filas = int(input("Número de filas: "))
columnas = int(input("Número de columnas: "))

matriz = []

for i in range(filas):
    fila = []
    for j in range(columnas):
        num = float(input(f"Elemento [{i+1}][{j+1}]: "))
        fila.append(num)
    matriz.append(fila)

print("Matriz ingresada:")
for i in range(filas):
    for j in range(columnas):
        print(matriz[i][j], end=" ")
    print()

```
```
Proceso ActividadResuelta7

    Definir filas, columnas, i, j Como Entero;
    Dimension matriz[50,50];

    Escribir "Número de filas:";
    Leer filas;

    Escribir "Número de columnas:";
    Leer columnas;

    Para i <- 1 Hasta filas Hacer
        Para j <- 1 Hasta columnas Hacer
            Escribir "Elemento [", i, "][", j, "]:";
            Leer matriz[i,j];
        FinPara
    FinPara

    Escribir "Matriz ingresada:";

    Para i <- 1 Hasta filas Hacer
        Para j <- 1 Hasta columnas Hacer
            Escribir Sin Saltar matriz[i,j], " ";
        FinPara
        Escribir "";
    FinPara

FinProceso

```

**Ejercicio 7.8**
Se desea permutar las filas I y J de una matriz (array) de dos dimensiones (M*N):M filas, N columnas.
```python
filas = int(input("Número de filas: "))
columnas = int(input("Número de columnas: "))

matriz = []

for i in range(filas):
    fila = []
    for j in range(columnas):
        fila.append(float(input(f"Elemento [{i+1}][{j+1}]: ")))
    matriz.append(fila)

for i in range(filas):
    suma = 0
    for j in range(columnas):
        suma += matriz[i][j]
    print(f"Suma fila {i+1}: {suma}")

```
```
Proceso ActividadResuelta8

    Definir filas, columnas, i, j Como Entero;
    Definir suma Como Real;
    Dimension matriz[50,50];

    Escribir "Número de filas:";
    Leer filas;

    Escribir "Número de columnas:";
    Leer columnas;

    Para i <- 1 Hasta filas Hacer
        Para j <- 1 Hasta columnas Hacer
            Leer matriz[i,j];
        FinPara
    FinPara

    Para i <- 1 Hasta filas Hacer
        suma <- 0;
        Para j <- 1 Hasta columnas Hacer
            suma <- suma + matriz[i,j];
        FinPara
        Escribir "Suma fila ", i, ": ", suma;
    FinPara

FinProceso

```


**Ejercicio  7.9**
Algoritmo que nos permita calcular la desviación estándar (SIGMA) de una lista de N números (N <= 15).
```python
filas = int(input("Número de filas: "))
columnas = int(input("Número de columnas: "))

matriz = []

for i in range(filas):
    fila = []
    for j in range(columnas):
        fila.append(float(input(f"Elemento [{i+1}][{j+1}]: ")))
    matriz.append(fila)

for j in range(columnas):
    suma = 0
    for i in range(filas):
        suma += matriz[i][j]
    print(f"Suma columna {j+1}: {suma}")

```
```
Proceso ActividadResuelta9

    Definir filas, columnas, i, j Como Entero;
    Definir suma Como Real;
    Dimension matriz[50,50];

    Escribir "Número de filas:";
    Leer filas;

    Escribir "Número de columnas:";
    Leer columnas;

    Para i <- 1 Hasta filas Hacer
        Para j <- 1 Hasta columnas Hacer
            Leer matriz[i,j];
        FinPara
    FinPara

    Para j <- 1 Hasta columnas Hacer
        suma <- 0;
        Para i <- 1 Hasta filas Hacer
            suma <- suma + matriz[i,j];
        FinPara
        Escribir "Suma columna ", j, ": ", suma;
    FinPara

FinProceso

```

**Ejercicio 7.10**
Utilizando arrays, escribir un algoritmo que visualice un cuadrado mágico de orden impar n, comprendido entre 3 y 11. El usuario debe elegir el valor de n.
Un cuadrado mágico se compone de números enteros comprendidos entre 1 y n. La suma de los números que figuran en cada fila, columna y diagonal son iguales.
```python
n = int(input("Tamaño de la matriz cuadrada: "))

matriz = []

for i in range(n):
    fila = []
    for j in range(n):
        if i == j:
            fila.append(1)
        else:
            fila.append(0)
    matriz.append(fila)

for fila in matriz:
    print(fila)

```
```
Proceso ActividadResuelta10

    Definir n, i, j Como Entero;
    Dimension matriz[50,50];

    Escribir "Tamaño de la matriz cuadrada:";
    Leer n;

    Para i <- 1 Hasta n Hacer
        Para j <- 1 Hasta n Hacer
            Si i = j Entonces
                matriz[i,j] <- 1;
            SiNo
                matriz[i,j] <- 0;
            FinSi
        FinPara
      FinPara

      Para i <- 1 Hasta n Hacer
        Para j <- 1 Hasta n Hacer
            Escribir Sin Saltar matriz[i,j], " ";
        FinPara
        Escribir "";
      FinPara

FinProceso

```


**Ejercicio 7.11**
Obtener un algoritmo que efectúe la multiplicación de dos matrices A, B
```python
filas = int(input("Número de filas: "))
columnas = int(input("Número de columnas: "))

matriz = []

for i in range(filas):
    fila = []
    for j in range(columnas):
        fila.append(float(input(f"Elemento [{i+1}][{j+1}]: ")))
    matriz.append(fila)

print("Matriz transpuesta:")

for j in range(columnas):
    for i in range(filas):
        print(matriz[i][j], end=" ")
    print()

```
```
Proceso ActividadResuelta11

    Definir filas, columnas, i, j Como Entero;
    Dimension matriz[50,50];

    Escribir "Número de filas:";
    Leer filas;

    Escribir "Número de columnas:";
    Leer columnas;

    Para i <- 1 Hasta filas Hacer
        Para j <- 1 Hasta columnas Hacer
            Leer matriz[i,j];
        FinPara
    FinPara

    Escribir "Matriz transpuesta:";

    Para j <- 1 Hasta columnas Hacer
        Para i <- 1 Hasta filas Hacer
            Escribir Sin Saltar matriz[i,j], " ";
        FinPara
        Escribir "";
    FinPara

FinProceso

```
**Ejercicio 7.12**
 Algoritmo que triangule una matriz cuadrada y halle su determinante. En las matrices cuadradas el valor del determinante coincide con el producto de los elementos de la diagonal de la matriz triangulada, multiplicado por –1
tantas veces como hayamos intercambiado filas al triangular la matriz.
Proceso de triangulación de una matriz para todo i desde 1 hasta n – 1 hacer:
a) Si el elemento de lugar (i,i) es nulo, intercambiar filas hasta que dicho elemento sea no nulo o agotar los
posibles intercambios.
b) A continuación se busca el primer elemento no nulo de la fila i-ésima y, en el caso de existir, se usa para
hacer ceros en la columna de abajo.
Estructuras de datos I (arrays y estructuras) 281
 Sea dicho elemento matriz[i,r]
 Multiplicar fila i por matriz[i+1,r]/matriz[i,r] y restarlo a la i+1
 Multiplicar fila i por matriz[i+2,r]/matriz[i,r] y restarlo a la i+2
 ............................................................................................................
 Multiplicar fila i por matriz[m,r]/matriz[i,r] y restarlo a la m.
```python
n = int(input("Tamaño de la matriz cuadrada: "))

# Cargar matriz
matriz = []
for i in range(n):
    fila = []
    for j in range(n):
        fila.append(float(input(f"Elemento [{i+1}][{j+1}]: ")))
    matriz.append(fila)

determinante = 1
intercambios = 0

# Eliminación Gaussiana
for i in range(n):
    # Si el pivote es 0, buscar intercambio
    if matriz[i][i] == 0:
        for k in range(i+1, n):
            if matriz[k][i] != 0:
                matriz[i], matriz[k] = matriz[k], matriz[i]
                intercambios += 1
                break

    pivote = matriz[i][i]

    if pivote != 0:
        for j in range(i+1, n):
            factor = matriz[j][i] / pivote
            for k in range(i, n):
                matriz[j][k] -= factor * matriz[i][k]

# Producto diagonal
for i in range(n):
    determinante *= matriz[i][i]

# Ajustar signo por intercambios
if intercambios % 2 != 0:
    determinante *= -1

print("Matriz triangular:")
for fila in matriz:
    print(fila)

print("Determinante:", determinante)

```
```
Proceso Ejercicio7_12;

    Definir n, i, j, k, intercambios Como Entero;
    Definir pivote, factor, determinante Como Real;
    Dimension matriz[20,20];

    Escribir "Tamaño de la matriz cuadrada:";
    Leer n;

    Para i <- 1 Hasta n Hacer
        Para j <- 1 Hasta n Hacer
            Escribir "Elemento [", i, "][", j, "]:";
            Leer matriz[i,j];
        FinPara
    FinPara

    determinante <- 1;
    intercambios <- 0;

    Para i <- 1 Hasta n Hacer

        Si matriz[i,i] = 0 Entonces
            Para k <- i+1 Hasta n Hacer
                Si matriz[k,i] <> 0 Entonces
                    Para j <- 1 Hasta n Hacer
                        pivote <- matriz[i,j];
                        matriz[i,j] <- matriz[k,j];
                        matriz[k,j] <- pivote;
                    FinPara
                    intercambios <- intercambios + 1;
                FinSi
            FinPara
        FinSi

        pivote <- matriz[i,i];

        Si pivote <> 0 Entonces
            Para j <- i+1 Hasta n Hacer
                factor <- matriz[j,i] / pivote;
                Para k <- i Hasta n Hacer
                    matriz[j,k] <- matriz[j,k] - factor * matriz[i,k];
                FinPara
            FinPara
        FinSi

    FinPara

    Para i <- 1 Hasta n Hacer
        determinante <- determinante * matriz[i,i];
    FinPara

    Si intercambios MOD 2 <> 0 Entonces
        determinante <- determinante * -1;
    FinSi

    Escribir "Matriz triangular:";
    Para i <- 1 Hasta n Hacer
        Para j <- 1 Hasta n Hacer
            Escribir Sin Saltar matriz[i,j], " ";
        FinPara
        Escribir "";
    FinPara

    Escribir "Determinante: ", determinante;

FinProceso

```

# Funciones(módulos):resolver los ejercicios propuestos y resueltos TODOS en PsInet y Python*
-----------
# EJERCICOS RESUELTOS

6.1. Realización del factorial de un número entero.

**Python**

```python
def factorial(n):
    f = 1
    if n == 0:
        return 1
    else:
        for i in range(1, n + 1):
            f *= i
        return f
num = int(input("Ingrese un número entero: "))
resultado = factorial(num)
print("El factorial es:", resultado)
```

**PSeInt**

```
Algoritmo Factorial
    Definir n, f, i Como Entero
    Escribir "Ingrese un número entero:"
    Leer n
    f <- 1
    Si n = 0 Entonces
        f <- 1
    Sino
        Para i <- 1 Hasta n Hacer
            f <- f * i
        FinPara
    FinSi
    Escribir "El factorial es:", f
FinAlgoritmo
```

6.2. Diseñar un algoritmo que calcule el máximo común divisor de dos números mediante el algoritmo de Euclides. Sean los dos números A y B. El método para hallar el máximo común divisor (mcd) de dos números A y B por el método de Euclides es: 1. Dividir el número mayor (A) por el menor (B). Si el resto de la división es cero, el número B es el máximo común divisor. 2. Si la división no es exacta, se divide el número menor (B) por el resto de la división anterior. 3. Se siguen los pasos anteriores hasta obtener un resto cero. El último divisor es el mcd buscado.

**Python**

```python
def mcd(a, b):
    while a != b:
        if a > b:
            a = a - b
        else:
            b = b - a
    return a
num1 = int(input("Ingrese el primer número: "))
num2 = int(input("Ingrese el segundo número: "))
resultado = mcd(num1, num2)
print("El máximo común divisor es:", resultado)
```

**PSeInt**

```
Algoritmo Maximo_Comun_Divisor
    Definir a, b Como Entero;

    Escribir "Ingrese el primer numero:";
    Leer a;

    Escribir "Ingrese el segundo numero:";
    Leer b;

    Mientras a <> b Hacer
        Si a > b Entonces
            a <- a - b;
        SiNo
            b <- b - a;
        FinSi
    FinMientras

    Escribir "El maximo comun divisor es: ", a;
FinAlgoritmo
```

6.3. Para calcular el máximo común divisor (mcd) de dos números se recurre a una función específica definida con un subprograma. Se desea calcular la salida del programa principal con dos números A y B, cuyos valores son 10 y 25, es decir, el mcd (A, B) y comprobar el método de paso de parámetros por valor.

**Python**

```python
def mcd(a, b):
    while a != b:
        if a > b:
            a = a - b
        else:
            b = b - a
    return a
x = 10
y = 25
n = mcd(x, y)
print(x, y, n)
```

**PSeInt**

```
Algoritmo MCD_PorValor
    Definir A, B, resultado Como Entero

    // Asignar valores a A y B
    A <- 10
    B <- 25

    // Llamar a la función que calcula el MCD
    resultado <- calcular_mcd(A, B)

    // Mostrar los resultados
    Escribir "El MCD de ", A, " y ", B, " es: ", resultado
FinAlgoritmo

// Función que recibe parámetros por valor
Funcion calcular_mcd(x, y) Como Entero
    Mientras x <> y Hacer
        Si x > y Entonces
            x <- x - y
        Sino
            y <- y - x
        FinSi
    FinMientras
    Retornar x
FinFuncion
```

6.4. Realizar un algoritmo que permita ordenar tres números mediante un procedimiento de intercambio en dos variables (paso de parámetros por referencia).

**Python**

```python
def intercambio(a, b):
    auxi = a
    a = b
    b = auxi
    return a, b
x = 132
y = 45
z = 15
if x > y:
    x, y = intercambio(x, y)
if y > z:
    y, z = intercambio(y, z)
if x > y:
    x, y = intercambio(x, y)
print(x, y, z)
```

**PSeInt**

```
Algoritmo Ordenar_Tres_Numeros
    Definir x Como Entero;
    Definir k Como Entero;
    Definir z Como Entero;
    Definir aux Como Entero;

    x <- 132;
    k <- 45;
    z <- 15;

    Si x > k Entonces
        aux <- x;
        x <- k;
        k <- aux;
    FinSi

    Si k > z Entonces
        aux <- k;
        k <- z;
        z <- aux;
    FinSi

    Si x > k Entonces
        aux <- x;
        x <- k;
        k <- aux;
    FinSi

    Escribir x, " ", k, " ", z;
FinAlgoritmo
```

6.5. Diseñar un algoritmo que llame a la función signo(X) y calcule: a) el signo de un número, b) el signo de la función coseno.

**Python**

```python
import math
def signo(x):
    if x > 0:
        return 1
    elif x < 0:
        return -1
    else:
        return 0
p = int(input("Ingrese un numero: "))
y = signo(p)
z = signo(math.cos(p))
print(y, z)
```

**PSeInt**

```
Algoritmo Signos
    Definir p Como Entero;
    Definir q Como Entero;
    Definir z Como Entero;
    Definir c Como Real;

    Escribir "Ingrese un numero:";
    Leer p;

    // Signo del numero
    Si p > 0 Entonces
        q <- 1;
    SiNo
        Si p < 0 Entonces
            q <- -1;
        SiNo
            q <- 0;
        FinSi
    FinSi

    // Coseno del numero
    c <- Cos(p);

    // Signo del coseno
    Si c > 0 Entonces
        z <- 1;
    SiNo
        Si c < 0 Entonces
            z <- -1;
        SiNo
            z <- 0;
        FinSi
    FinSi

    Escribir q, " ", z;
FinAlgoritmo
```


# EJERCICOS PROPUESTOS

6.1. Diseñar una función que calcule la media de tres números leídos del teclado y poner un ejemplo de su
aplicación.

**Python**

```python
def media(a, b, c):
    return (a + b + c) / 3
x = int(input("Ingrese el primer número: "))
k = int(input("Ingrese el segundo número: "))
z = int(input("Ingrese el tercer número: "))
resultado = media(x, k, z)
print("La media es:", resultado)
```

**PSeInt**

```
Algoritmo Media_Tres_Numeros
    Definir x Como Entero;
    Definir k Como Entero;
    Definir z Como Entero;
    Definir media Como Real;

    Escribir "Ingrese el primer numero:";
    Leer x;

    Escribir "Ingrese el segundo numero:";
    Leer k;

    Escribir "Ingrese el tercer numero:";
    Leer z;

    media <- (x + k + z) / 3;

    Escribir "La media es: ", media;
FinAlgoritmo
```

6.2. Diseñar la función FACTORIAL que calcule el factorial
de un número entero en el rango 100 a 1.000.000.

**Python**

```python
def factorial(n):
    f = 1
    i = 1
    while i <= n:
        f = f * i
        i = i + 1
    return f
n = int(input("Ingrese un número entero: "))
if n >= 100 and n <= 1000000:
    resultado = factorial(n)
    print("El factorial es:", resultado)
else:
    print("El número no está en el rango permitido")
```

**PSeInt**

```
Algoritmo Factorial_Rango
    Definir n Como Entero;
    Definir i Como Entero;
    Definir f Como Entero;

    Escribir "Ingrese un numero entero:";
    Leer n;

    Si n >= 100 Y n <= 1000000 Entonces
        f <- 1;
        i <- 1;

        Mientras i <= n Hacer
            f <- f * i;
            i <- i + 1;
        FinMientras

        Escribir "El factorial es: ", f;
    SiNo
        Escribir "El numero no esta en el rango permitido";
    FinSi
FinAlgoritmo
```

6.3. Diseñar un algoritmo para calcular el máximo común
divisor de cuatro números basado en un subalgoritmo función mcd (máximo común divisor de dos números).

**Python**

```python
def mcd(a, b):
    while a != b:
        if a > b:
            a = a - b
        else:
            b = b - a
    return a
n1 = int(input("Ingrese el primer número: "))
n2 = int(input("Ingrese el segundo número: "))
n3 = int(input("Ingrese el tercer número: "))
n4 = int(input("Ingrese el cuarto número: "))
resultado = mcd(n1, n2)
resultado = mcd(resultado, n3)
resultado = mcd(resultado, n4)
print("El máximo común divisor es:", resultado)
```

**PSeInt**

```
Algoritmo MCD_Cuatro_Numeros
    Definir n1 Como Entero;
    Definir n2 Como Entero;
    Definir n3 Como Entero;
    Definir n4 Como Entero;
    Definir a Como Entero;
    Definir b Como Entero;

    Escribir "Ingrese el primer numero:";
    Leer n1;
    Escribir "Ingrese el segundo numero:";
    Leer n2;
    Escribir "Ingrese el tercer numero:";
    Leer n3;
    Escribir "Ingrese el cuarto numero:";
    Leer n4;

    // MCD de n1 y n2
    a <- n1;
    b <- n2;
    Mientras a <> b Hacer
        Si a > b Entonces
            a <- a - b;
        SiNo
            b <- b - a;
        FinSi
    FinMientras
    n1 <- a;

    // MCD del resultado con n3
    a <- n1;
    b <- n3;
    Mientras a <> b Hacer
        Si a > b Entonces
            a <- a - b;
        SiNo
            b <- b - a;
        FinSi
    FinMientras
    n1 <- a;

    // MCD del resultado con n4
    a <- n1;
    b <- n4;
    Mientras a <> b Hacer
        Si a > b Entonces
            a <- a - b;
        SiNo
            b <- b - a;
        FinSi
    FinMientras

    Escribir "El maximo comun divisor es: ", a;
FinAlgoritmo
```

6.4. Diseñar una función que encuentre el mayor de dos
números enteros.

**Python**

```python
def mayor(a, b):
    if a > b:
        return a
    else:
        return b
x = int(input("Ingrese el primer número: "))
z = int(input("Ingrese el segundo número: "))
resultado = mayor(x, z)
print("El número mayor es:", resultado)
```

**PSeInt**

```
Algoritmo Mayor_De_Dos
    Definir x Como Entero;
    Definir z Como Entero;
    Definir mayor Como Entero;

    Escribir "Ingrese el primer numero:";
    Leer x;

    Escribir "Ingrese el segundo numero:";
    Leer z;

    Si x > z Entonces
        mayor <- x;
    SiNo
        mayor <- z;
    FinSi

    Escribir "El numero mayor es: ", mayor;
FinAlgoritmo
```

6.5. Diseñar una función que calcule xn para x, variable
real y n variable entera.

**Python**

```python
def potencia(x, n):
    resultado = 1
    i = 1
    while i <= n:
        resultado = resultado * x
        i = i + 1
    return resultado
x = int(input("Ingrese el valor de x: "))
n = int(input("Ingrese el valor de n: "))
print("La potencia es:", potencia(x, n))
```

**PSeInt**

```
Algoritmo Potencia
    Definir x Como Entero;
    Definir n Como Entero;
    Definir i Como Entero;
    Definir resultado Como Entero;

    Escribir "Ingrese el valor de x:";
    Leer x;

    Escribir "Ingrese el valor de n:";
    Leer n;

    resultado <- 1;
    i <- 1;

    Mientras i <= n Hacer
        resultado <- resultado * x;
        i <- i + 1;
    FinMientras

    Escribir "El resultado es: ", resultado;
FinAlgoritmo
```

6.6. Diseñar un procedimiento que acepte un número de
mes, un número de día y un número de año y los visualice en el formato
dd/mm/aa
 Por ejemplo, los valores 19,09,1987 se visualizarían
como
19/9/87
 y para los valores 3, 9 y 1905
3/9/05

**Phyton**

```python
# Algoritmo FormatoFecha en Python sin funciones especiales

# Definir variables
dia = 0
mes = 0
anio = 0
anio2 = 0
texto_anio = ""

# Pedir datos al usuario
print("Ingrese el día:")
dia = int(input())
print("Ingrese el mes:")
mes = int(input())
print("Ingrese el año:")
anio = int(input())

# Obtener los dos últimos dígitos del año
anio2 = anio % 100

# Convertir a texto y agregar cero delante si es menor a 10
if anio2 < 10:
    texto_anio = "0" + str(anio2)
else:
    texto_anio = str(anio2)

# Mostrar la fecha en formato dd/mm/aa
print(str(dia) + "/" + str(mes) + "/" + texto_anio)
```

**Pseint**

```
Algoritmo ejercicio6_6_FormatoFecha
    Definir dia, mes, anio, anio2 Como Entero
    Definir texto_anio Como Cadena

    Escribir "Ingrese el día:"
    Leer dia
    Escribir "Ingrese el mes:"
    Leer mes
    Escribir "Ingrese el año:"
    Leer anio

    // Obtener los dos últimos dígitos del año
    anio2 <- anio MOD 100

    // Convertir a texto y agregar cero delante si es menor a 10
    Si anio2 < 10 Entonces
        texto_anio <- "0" + ConvertirATexto(anio2)
    Sino
        texto_anio <- ConvertirATexto(anio2)
    FinSi

    // Mostrar la fecha en formato dd/mm/aa
    Escribir ConvertirATexto(dia) + "/" + ConvertirATexto(mes) + "/" + texto_anio
FinAlgoritmo
```

6.7. Realizar un procedimiento que realice la conversión
de coordenadas polares (r, θ) a coordenadas cartesianas (x, y)
x = r.cos (θ)
y = r.sen(θ)

**Phyton**

```python
# Conversión de coordenadas polares a cartesianas

# Definir variables
r = 0.0
theta = 0.0
x = 0.0
y = 0.0
radianes = 0.0

# Pedir datos al usuario
print("Ingrese el valor de r:")
r = float(input())
print("Ingrese el angulo theta en grados:")
theta = float(input())

# Convertir grados a radianes
radianes = theta * 3.14159265 / 180

# Calcular coordenadas cartesianas
x = r * ( (3.14159265/180) * theta ) # Esto era para mostrar la idea
# Pero necesitamos coseno y seno, sin funciones de Python, podemos usar aproximaciones


import math  # Solo si podemos usar funciones matemáticas básicas
x = r * math.cos(radianes)
y = r * math.sin(radianes)

# Mostrar resultados
print("Coordenadas cartesianas:")
print("x =", x)
print("y =", y)
```

**Pseint**

```
Algoritmo PolaresACartesianas

    // Definir variables
    Definir r, theta, x, f, radianes Como Real

    Escribir "Ingrese el valor de r:"
    Leer r
    Escribir "Ingrese el angulo theta en grados:"
    Leer theta

    // Convertir grados a radianes
    radianes <- theta * 3.14159265 / 180

    // Calcular coordenadas cartesianas
    x <- r * cos(radianes)
    f <- r * sen(radianes)

    // Mostrar resultados
    Escribir "Coordenadas cartesianas:"
    Escribir "x = ", x
    Escribir "y = ", f

FinAlgoritmo
```

6.8. Escribir una función Salario que calcule los sa larios
de un trabajador para un número dado de horas trabajadas y un salario hora. Las horas que su peren las 40
horas semanales se pagarán como extras con un salario hora 1,5 veces el salario ordinario.

Phyton

```python
# Función para calcular salario con horas extras
def calcular_salario(horas, salario_hora):
    if horas > 40:
        horas_extra = horas - 40
        salario_total = 40 * salario_hora + horas_extra * salario_hora * 1.5
    else:
        salario_total = horas * salario_hora
    return salario_total

# Pedir datos al usuario
horas = float(input("Ingrese el número de horas trabajadas: "))
salario_hora = float(input("Ingrese el salario por hora: "))

# Calcular salario usando la función
salario_total = calcular_salario(horas, salario_hora)

# Mostrar el resultado
print("El salario total es:", salario_total)
```

**Pseint**

```
Algoritmo CalcularSalario

    // Definir variables
    Definir horas, salarioHora, salarioTotal, horasExtra Como Real

    // Pedir datos al usuario
    Escribir "Ingrese el número de horas trabajadas:"
    Leer horas
    Escribir "Ingrese el salario por hora:"
    Leer salarioHora

    // Calcular salario
    Si horas > 40 Entonces
        horasExtra <- horas - 40
        salarioTotal <- 40 * salarioHora + horasExtra * salarioHora * 1.5
    Sino
        salarioTotal <- horas * salarioHora
    FinSi

    // Mostrar resultado
    Escribir "El salario total es: ", salarioTotal

FinAlgoritmo
```

6.9. Escribir una función booleana Digito que determine
si un carácter es uno de los dígitos 0 al 9.

**Phyton**

```python
# Función que verifica si un carácter es un dígito
def es_digito(c):
    return c in "0123456789"

# Pedir carácter al usuario
c = input("Ingrese un carácter: ")

# Verificar si es dígito usando la función
if es_digito(c):
    print("El carácter es un dígito.")
else:
    print("El carácter NO es un dígito.")
```

**Pseint**

```
Algoritmo DigitoEjemplo

    Definir c Como Caracter
    Definir esDigito Como Entero

    Escribir "Ingrese un carácter:"
    Leer c

    // Comprobar si es un dígito
    Si c = "0" O c = "1" O c = "2" O c = "3" O c = "4" O c = "5" O c = "6" O c = "7" O c = "8" O c = "9" Entonces
        esDigito <- 1
    Sino
        esDigito <- 0
    FinSi

    // Mostrar resultado
    Si esDigito = 1 Entonces
        Escribir "El carácter es un dígito."
    Sino
        Escribir "El carácter NO es un dígito."
    FinSi

FinAlgoritmo
```

6.10. Diseñar una función que permita devolver el valor absoluto de un número.

**Phyton**

```python
# Función que devuelve el valor absoluto
def valor_absoluto(n):
    if n < 0:
        return -n
    else:
        return n

# Pedir número al usuario
num = float(input("Ingrese un número: "))

# Calcular valor absoluto usando la función
resultado = valor_absoluto(num)

# Mostrar el resultado
print("El valor absoluto es:", resultado)
```

**Pseint**

```
Algoritmo ValorAbsolutoSeguro

    Definir num, resultado Como Real

    Escribir "Ingrese un número:"
    Leer num

    // Calcular valor absoluto
    Si num < 0 Entonces
        resultado <- -num
    Sino
        resultado <- num
    FinSi

    Escribir "El valor absoluto es: ", resultado

FinAlgoritmo
```

6.11. Realizar un procedimiento que obtenga la división entera y el resto de la misma utilizando únicamente los
operadores suma y resta.

**Phyton**

```python
# Pedir datos al usuario
dividendo = int(input("Ingrese el dividendo: "))
divisor = int(input("Ingrese el divisor: "))

# Inicializar cociente y acumulador
cociente = 0
acumulador = dividendo

# Restar el divisor repetidamente hasta que el acumulador sea menor que divisor
while acumulador >= divisor:
    acumulador -= divisor  # equivalente a acumulador = acumulador - divisor
    cociente += 1          # aumentar cociente en 1

# Lo que queda en acumulador es el resto
resto = acumulador

# Mostrar resultados
print("Cociente:", cociente)
print("Resto:", resto)
```

**Pseint**

```
Algoritmo DivisionEnteraYSobreSeguro

    Definir dividendo, divisor, cociente, resto, acumulador Como Entero

    Escribir "Ingrese el dividendo:"
    Leer dividendo
    Escribir "Ingrese el divisor:"
    Leer divisor

    cociente <- 0
    acumulador <- dividendo

    // Restar divisor repetidamente hasta que el acumulador sea menor que divisor
    Mientras acumulador >= divisor Hacer
        acumulador <- acumulador - divisor
        cociente <- cociente + 1
    FinMientras

    // Lo que queda es el resto
    resto <- acumulador

    // Mostrar resultados
    Escribir "Cociente:", cociente
    Escribir "Resto:", resto

FinAlgoritmo
```

6.12. Escribir una función que permita deducir si una fecha
leída del teclado es válida.

**Phyton**

```python
# Función que verifica si una fecha es válida
def es_fecha_valida(dia, mes, anio):
    # Comprobar mes válido
    if mes < 1 or mes > 12:
        return False

    # Determinar número de días según el mes
    if mes in [1, 3, 5, 7, 8, 10, 12]:
        dias_mes = 31
    elif mes in [4, 6, 9, 11]:
        dias_mes = 30
    else:  # Febrero
        # Año bisiesto: divisible por 4 y (no divisible por 100 o divisible por 400)
        if (anio % 4 == 0) and ((anio % 100 != 0) or (anio % 400 == 0)):
            dias_mes = 29
        else:
            dias_mes = 28

    # Comprobar día válido
    if dia < 1 or dia > dias_mes:
        return False

    return True

# Pedir fecha al usuario
dia = int(input("Ingrese el día: "))
mes = int(input("Ingrese el mes: "))
anio = int(input("Ingrese el año: "))

# Validar la fecha usando la función
if es_fecha_valida(dia, mes, anio):
    print("La fecha es válida.")
else:
    print("La fecha NO es válida.")
```

**Pseint**

```
Algoritmo FechaValidaSeguro

    Definir dia, mes, anio, diasMes, fechaValida Como Entero

    Escribir "Ingrese el día:"
    Leer dia
    Escribir "Ingrese el mes:"
    Leer mes
    Escribir "Ingrese el año:"
    Leer anio

    fechaValida <- 1  // 1 = verdadero, 0 = falso

    // Verificar mes válido
    Si mes < 1 O mes > 12 Entonces
        fechaValida <- 0
    FinSi

    // Determinar número de días según el mes
    Si fechaValida = 1 Entonces
        Si mes = 1 O mes = 3 O mes = 5 O mes = 7 O mes = 8 O mes = 10 O mes = 12 Entonces
            diasMes <- 31
        Sino
            Si mes = 4 O mes = 6 O mes = 9 O mes = 11 Entonces
                diasMes <- 30
            Sino
                // Febrero
                Si (anio MOD 4 = 0) Y ((anio MOD 100 <> 0) O (anio MOD 400 = 0)) Entonces
                    diasMes <- 29
                Sino
                    diasMes <- 28
                FinSi
            FinSi
        FinSi
    FinSi

    // Verificar día válido
    Si fechaValida = 1 Entonces
        Si dia < 1 O dia > diasMes Entonces
            fechaValida <- 0
        FinSi
    FinSi

    // Mostrar resultado
    Si fechaValida = 1 Entonces
        Escribir "La fecha es válida."
    Sino
        Escribir "La fecha NO es válida."
    FinSi

FinAlgoritmo
```

6.13. Diseñar un algoritmo que transforme un número introducido por teclado en notación decimal a notación
romana. El número será entero positivo y no excederá
de 3.000.

**Phyton**

```python
n = int(input("Ingrese un numero (1 a 3000): "))

if n < 1 or n > 3000:
    print("Numero fuera de rango")
else:
    while n >= 1000:
        print("M", end="")
        n -= 1000

    while n >= 500:
        print("D", end="")
        n -= 500

    while n >= 100:
        print("C", end="")
        n -= 100

    while n >= 50:
        print("L", end="")
        n -= 50

    while n >= 10:
        print("X", end="")
        n -= 10

    while n >= 5:
        print("V", end="")
        n -= 5

    while n >= 1:
        print("I", end="")
        n -= 1
```

**Pseint**

```
Algoritmo DecimalARomano
	Definir n Como Entero

	Escribir "Ingrese un numero (1 a 3000):"
	Leer n

	Si n < 1 O n > 3000 Entonces
		Escribir "Numero fuera de rango"
	SiNo

		Mientras n >= 1000 Hacer
			Escribir Sin Saltar "M"
			n <- n - 1000
		FinMientras

		Mientras n >= 500 Hacer
			Escribir Sin Saltar "D"
			n <- n - 500
		FinMientras

		Mientras n >= 100 Hacer
			Escribir Sin Saltar "C"
			n <- n - 100
		FinMientras

		Mientras n >= 50 Hacer
			Escribir Sin Saltar "L"
			n <- n - 50
		FinMientras

		Mientras n >= 10 Hacer
			Escribir Sin Saltar "X"
			n <- n - 10
		FinMientras

		Mientras n >= 5 Hacer
			Escribir Sin Saltar "V"
			n <- n - 5
		FinMientras

		Mientras n >= 1 Hacer
			Escribir Sin Saltar "I"
			n <- n - 1
		FinMientras

	FinSi

FinAlgoritmo
```

6.14. Escribir el algoritmo de una función recursiva que: a)
calcule el factorial de un número entero positivo, b) la
potencia de un número entero positivo.

**Phyton**

```python
# factorial recursivo
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)


# potencia recursiva
def potencia(base, exponente):
    if exponente == 0:
        return 1
    else:
        return base * potencia(base, exponente - 1)


# programa principal
n = int(input("Ingrese un numero para calcular el factorial: "))
print("El factorial es:", factorial(n))

b = int(input("Ingrese la base: "))
e = int(input("Ingrese el exponente: "))
print("La potencia es:", potencia(b, e))
```

**Pseint**

```
SubProceso factorial(n, resultado Por Referencia)
    Si n = 0 Entonces
        resultado <- 1
    Sino
        factorial(n - 1, resultado)
        resultado <- n * resultado
    FinSi
FinSubProceso


SubProceso potencia(base, exponente, resultado Por Referencia)
    Si exponente = 0 Entonces
        resultado <- 1
    Sino
        potencia(base, exponente - 1, resultado)
        resultado <- base * resultado
    FinSi
FinSubProceso


Algoritmo Recursividad

    Definir n, b, e Como Entero
    Definir resFactorial, resPotencia Como Entero

    Escribir "Ingrese un numero para calcular el factorial:"
    Leer n
    factorial(n, resFactorial)
    Escribir "El factorial es: ", resFactorial

    Escribir "Ingrese la base:"
    Leer b
    Escribir "Ingrese el exponente:"
    Leer e
    potencia(b, e, resPotencia)
    Escribir "La potencia es: ", resPotencia

FinAlgoritmo
```
