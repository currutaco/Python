# 6 Práctica 
Sentencias condicionales. (6 puntos)

## Ejercicio 1 (1.5 puntos)
Realizar un ejemplo de menú, donde podemos escoger las distintas opciones
hasta que seleccionamos la opción de “Salir”.

Menú de recomendaciones
1. Literatura
2. Cine
3. Música
4. Videojuegos
5. Salir

### Al ingresar una opcion
opcion 1:

Lecturas recomendables:

* Esperándolo a Tito y otros cuentos de fútbol (Eduardo
Sacheri)
* El juego de Ender (Orson Scott Card)
* El sueño de los héroes (Adolfo Bioy Casares)

opcion 2:

Películas recomendables:

* Matrix (1999)
* El último samuray (2003)
* Cars (2006)

opcion  3:

Discos recomendables:

* Despedazado por mil partes (La Renga, 1996)
* Búfalo (La Mississippi, 2008)
* Gaia (Mago de Oz, 2003)

opcion 4:

* Videojuegos clásicos recomendables
* Día del tentáculo (LucasArts, 1993)
* Terminal Velocity (Terminal Reality/3D Realms, 1995)
* Death Rally (Remedy/Apogee, 1996)

opcion  5:

Gracias, vuelva prontos

Opción no válida, en caso de ingresar un número fuera de las opciones

print("""Menú

1-Literatura

2-Cine

3-Música

4-Videojuegos

5-Salir"""

)


opcion=int(input('\nPor favor seleccione una opción: ') )


if opcion == 1:

    print("""
    
    Lecturas recomendables:
    
    
    Esperando a Tito y otros cuentos de fútbol (Eduardo Sacheri)
    El juego de Ender (Orson Scott Card)
    El sueño de los héroes (Adolfo Bioy Casares)""")
    
elif opcion == 2:

    print(""" 
    
    Películas recomendables:
    
    
    Matrix (1999)
    El último samurai (2003)
    Cars (2006)""")
    
elif opcion == 3:

    print("""   
    
    Discos recomendables:
    

    Despedazado por mil partes (La Renga, 1996)
    Búfalo (La Mississippi, 2008)
    Gaia (Mago de Oz, 2003)""")
    
elif opcion == 4:

    print("""
    
    Videojuegos clásicos recomendables:
    
    
    Día del tentáculo (LucasArts, 1993)
    Terminal Velocity (Terminal Reality/3D Realms, 1995)
    Death Rally (Remedy/Apogee, 1996)""")
    
elif opcion == 5:

    print("Gracias, vuelva pronto")
    
else:

    print('Opción no válida')
    



## Ejercicio 2 (1.5 puntos)
Se pide por teclado un número y nos imprime los números primos que hay previos a este número.

Ejemplo: si ingresamos el 10 nos imprima del 1 a ese 10 cuales números son primos.


n1=int(input('Ingresa un número: '))
l =[]

for i in range(3,n1+1):

    for j in range (2, i):
    
        if i%j == 0:
        
            break
            
    else:
    
        l.append(i)
        
print (l)  


## Ejercicio 3 (1.5 puntos)
Una persona adquirió un producto para pagar en 20 meses. El primer mes pagó
10 €, el segundo 20 €, el tercero 40 € y así sucesivamente. Realizar un algoritmo
para determinar cuánto debe pagar mensualmente y el total de lo que pagó
después de los 20 meses.


El ejercicio solo pide un algoritmo, no un código o algo por el estilo. La idea sería así:

Al finalizar los 20 meses pago en total:

primer mes pago 10, segundo mes pago 20, tercer mes pago 30, cuarto mes pago 40, etc.

El total estará dado por:

    10+20+40+80+...
    
    
lo cual puede escribirse como:

    10(1+2+4+8+...)
    
o bien:

    10 (sumatoria de 2**n)
    
    
donde n empieza desde cero hasta 19. Es decir que el algoritmo sería hacer un programa que para un índice dado ( donde el índice es el número de mes)
calcule lo que hay que pagar y sume lo acumulado hasta ése mes.

Esto se puede lograr haciendo un programa para tal efecto:

mes = int(input('Ingresa el numero de mes a calcular: ') )

inte = []

for i in range(0,mes):

    interes = 10*(2**i)
    
    inte.append(interes)
    
    print('Mes',i+1, 'pago: ',inte[i])
    
print('Pago total: ', 10*(2**19) )


