# 5 Práctica 5. Operadores relacionales. (6 puntos) 
### 5.1 Ejercicio 1 (2 puntos)
Programa que imprima si el número es positivo o negativo, el número debe ser ingresado por consola.

num =int(input("Ingresa un número: ") )


if num>0:

    print('El número es positivo')
    
    
if num<0:

    print('El número es negativo')
    
elif num==0:

    print('El número no es positivo ni negativo')

### 5.2 Ejercicio 2 (2 puntos)
Programa que imprima si el número ingresado esta en el rango de 1 a 7, el número se solicita por consola.

n = int(input('Ingresa un número: '))


if n in range(1,8):

    print('El número se encuentra en el rango de 1 a 7')
    
    
else:

    print('El número no se encuentra en el rango de 1 a 7')
    

### 5.3 Ejercicio 3 (2 puntos)
Programa que solicite un monto y que solicite el interés mensual, si el interés es mayor al 30% nos imprimirá que es incorrecto, si es menor realizará el cálculo e imprimira el monto con su interés adicionado.

m = int(input('Ingresa el monto: '))

n = int(input('Ingresa el interés mensual: '))


total = m*(1+(n/100))


if n>30:

    print('Incorrecto')
    
    
else:

    print(f'El monto total es: {total}')
