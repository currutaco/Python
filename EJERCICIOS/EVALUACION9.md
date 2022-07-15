# Práctica 9. Programación funcional. (6 puntos)
## Ejercicio 1 (2 puntos)
Realice un programa que pregunte aleatoriamente una multiplicación. El programa
debe indicar si la respuesta ha sido correcta o no (en caso que la respuesta sea
incorrecta el programa debe indicar cuál es la correcta). El programa preguntará
10 multiplicaciones, y al finalizar mostrará el número de aciertos.

#### Análisis
* Hacemos un bucle con 10 iteraciones, en cada iteración se inicializan dos
números con un valor aleatorio (de 2 a 10). Se calcula la multiplicación.
* Mostramos la multiplicación, y pedimos por teclado el resultado. Si
coincide con la multiplicación calculada cuento un acierto, sino escribimos un
mensaje de error mostrando el resultado correcto. Cuando salimos del bucle
mostramos el número de aciertos.

Ejemplo. imprime una multiplicacion (9 * 8 =  )por teclado se ingresa la respuesta, eso pasa 10 veces y al final nos imprime cuantas respuestas fueron correctas

Recuerda el import random


import random


intentos = 0

acierto = 0

error = 0

while intentos<10:

  x = random.randint(2,10)
  
  y = random.randint(2,10)

  intentos= intentos +1
  
  mult = int(input(f'\nLa multiplicación {x}*{y} es igual a: '))
 
 if mult==x*y:
 
    print('Respuesta correcta')
    
    acierto=acierto+1
    
  else:
  
    print('Respuesta incorrecta. La respuesta correcta es:',x*y)
    
    error=error+1
    

print('\nAciertos: ',acierto)

print('Errores: ', error)    




## Ejercicio 2 (2 puntos)
Obtener el cuadrado de todos los elementos en la lista.

Lista: [1,2,3,4,5,6,7,8,9,10]


lista=[1,2,3,4,5,6,7,8,9,10]


d=[n**2 for n in lista ]


print(d)


## Ejercicio 3 (2 puntos)
Obtener la cantidad de elementos mayores a 5 en la tupla.

tupla = (5,2,6,7,8,10,77,55,2,1,30,4,2,3)

def filtro(x):

  if x>5:
  
    return True
    
  else:
  
    return False
    

mayor= filter(filtro,tupla)


for x in mayor:

  print(x)


## Ejercicio 4 (2 puntos)
Obtener la suma de todos los elementos en la lista

from functools import reduce  


  def add(x, y):
  
      return x + y
      

  lista = [1,2,3,4]
  
  print(reduce(add, lista))
