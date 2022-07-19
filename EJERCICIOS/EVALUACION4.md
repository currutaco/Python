# Práctica 4. 6 puntos
## Tipos de colección de datos.
### 4.1 Ejercicio 1(1.2 puntos)
Realizar un programa que inicialice una lista con 10 valores aleatorios (del 1 al 10)
y posteriormente muestre en pantalla cada elemento de la lista junto con su
cuadrado y su cubo.
Respuesta:

import random
l=[]

for i in range(1,11):
    
    i = random.randint(1,10)

    l.append(i)

m=[m**2 for m in l]

n=[m**3 for m in l]

print('numeros:', l)

print('cuadrados:', m)

print('cubos:', n)

### 4.2 Ejercicio 2 (1.2 puntos)
Crea una lista e inicializarla con 5 cadenas de caracteres leídas por teclado. Copia
los elementos de la lista en otra lista pero en orden inverso, y muestra sus
elementos por la pantalla.

l=[]

n=0

while n<5:

    n = n+1
    
    p = input('Ingresa una palabra: ')

    l.append(p)

print(l)

print(l[::-1])

### 4.3 Ejercicio 3 (1.2 puntos)
Se quiere realizar un programa que lea por teclado las 5 notas obtenidas por un
alumno (comprendidas entre 0 y 10). A continuación debe mostrar todas las notas,
la nota media, la nota más alta que ha sacado y la menor.

l=[]

n=0

while n<5:

    n = n+1
    
    
    p = int(input('Ingresa una calificación: ') )
    

    l.append(p)
    
    
print('Calificación máxima: ', max(l))

print('Calificación mínima: ', min(l))

import statistics

print('Calificación media: ', statistics.mean(l))

### 4.4 Ejercicio 4 (1.2 puntos)
Codifica un programa en python que nos permita guardar los nombres de los
alumnos de una clase y las notas que han obtenido. Cada alumno puede tener
distinta cantidad de notas. Guarda la información en un diccionario cuya claves
serán los nombres de los alumnos y los valores serán listados con las notas de
cada alumno.

El programa pedirá el número de alumnos que vamos a introducir, pedirá su
nombre e irá pidiendo sus notas hasta que introduzcamos un número negativo. Al
final el programa nos mostrará la lista de alumnos y la nota media obtenida por
cada uno de ellos. Nota: si se introduce el nombre de un alumno que ya existe el
programa nos dará un error.

import statistics

al =[]

dicc={}

vuelta = 0

no_al = int(input('Ingresa el número de personas a considerar:  '))

while vuelta<no_al: 

    vuelta = vuelta +1
    
    a = input('\nIngresa el nombre de la persona: ')
    
    if a in al:
    
        print('Error. Esa persona ya existe')
        
    for i in range(no_al):
    
            dicc[f'{a}']=[]    
        
    else:
           al.append(a)
    
    n = int( input('Ingresa la(s) calificacion(es). Finaliza con un número negativo. ') )
    
    while n > 0:
            
        dicc[f'{a}'].append(n) 
            
        n = int( input('Ingresa la(s) calificacion(es). Finaliza con un número negativo. ') ) 
        
print('\nRelación de alumnos con sus notas medias')

for key, value in dicc.items():

    print('\n',key.title(),':',round(statistics.mean(value),3) )
    

### 4.5 Ejercicio 5 (1.2 puntos)
Crea una tupla con los meses del año, pide números al usuario, si el número está
entre 1 y la longitud máxima de la tupla, muestra el contenido de esa posición sino
muestra un mensaje de error. El programa termina cuando el usuario introduce un
cero.

meses = ('enero','febrero', 'marzo', 'abril', 'mayo', 'junio', 'julio','agosto','septiembre','octubre', 'noviembre', 'diciembre')


print('Este programa da el mes de acuerdo a un número. Finaliza introduciendo 0')

mes = int( input('Ingresa un número: ') )

if mes > len(meses):

    print('Error, el número es mayor al número de meses del año')
    

elif mes ==0:

    print('Fin')    
    
else:

    print('El mes correspondiente es: ',meses[mes-1])


# TRATA DE RESOLVER Y AVANZAR LO MÁS POSIBLE EN LOS EJERICICIOS, EL MARTES HABILITO "AYUDAS" EN CADA EJERCICIO
