# Práctica 8. (6 puntos)
## Ejercicio 1 (2 puntos)
Escribe un programa python que pida un número por teclado y que cree un
diccionario cuyas claves sean desde el número 1 hasta el número indicado, y los
valores sean los cuadrados de las claves.

Ejemplo: si se ingresa el 4 imprima el cuadrado de 1, de 2, de 3 y de 4

lim = int(input('ingresa un numero: '))


d = {n: n**2 for n in range(1,lim+1)}


print(d)



## Ejercicio 2 (2 puntos)
Escribe un programa que lea una cadena y devuelva un diccionario con la
cantidad de apariciones de cada carácter en la cadena.

Ejemplo: si se ingresa "paloma" p=1 a=2 l=1 o=1 m=1

l=[]

palabra = list(input('Ingresa una palabra: '))

for letra in palabra:

    
    cuenta = palabra.count(letra)
    
    l.append(cuenta)
    

dicc = dict(zip(palabra,l))


print(dicc)



## Ejercicio 3 (2 puntos)
Vamos a crear un programa en python donde vamos a declarar un diccionario para
guardar los precios de las distintas frutas. El programa pedirá el nombre de la fruta
y la cantidad que se ha vendido y nos mostrará el precio final de la fruta a partir de
los datos guardados en el diccionario. Si la fruta no existe nos dará un error. Tras
cada consulta el programa nos preguntará si queremos hacer otra consulta.




precios = {'melon':20,'guayaba':17, 'sandía':25, 'mango':15}


while True:

    
    fruta = input('\nIngrese el nombre de la fruta: ')
    
    cant = int(input('Ingrese la cantidad de fruta: '))
    
    
    if fruta not in precios:
    
        print('Error, fruta no encontrada')
        
        
    else:
    
        
        print('El precio final es: ', precios.get(fruta.lower())*cant )
        

        sn= input('\n ¿Desea hacer otra consulta? (s/n)')
        
    
        while sn.lower()!="s" and sn.lower() != "n":
        
            
            sn= input('\n ¿Desea hacer otra consulta? (s/n)')
            
        
        if sn.lower()=="n":
        
            break

