# Práctica 7. Programación orientada a objetos. (6 puntos)
## Ejercicio 1 (2 puntos)
Vamos a crear una clase llamada Persona. Sus atributos son: nombre, edad y
DNI. Construye los siguientes métodos para la clase:

● Un constructor, donde los datos pueden estar vacíos.

● Los setters y getters para cada uno de los atributos. Hay que validar las
entradas de datos.

● mostrar(): Muestra los datos de la persona.

● esMayorDeEdad(): Devuelve un valor lógico indicando si es mayor de edad.

class Persona:

    
    def __init__(self, nombre, edad, dni):
        
        self._nombre = nombre
        self._edad = edad
        self._dni = dni
        
    def get_Nombre(self):
        return self._nombre
        
    def set_Nombre(self, otro_nombre):
        self._nombre = otro_nombre
            
    def get_edad(self):
        return self._edad
        
    def set_edad(self, otra_edad):
        self._edad = otra_edad
        
    def get_dni(self):
        return self._dni
        
    def set_dni(self, otro_dni):
        self._dni = otro_dni
        
    def mostrar(self):
        print('El nombre es:',self.get_Nombre())
        print('La edad es: ',self.get_edad())
        print('El dni es: ', self.get_dni())
        
    def esMayorDeEdad(self):
        if int(self._edad) >=18:
            print(int(self._edad)>=18 )



## Ejercicio 2 (2 puntos)
Crea una clase llamada Cuenta que tendrá los siguientes atributos: titular (que es
una persona) y cantidad (puede tener decimales). El titular será obligatorio y la
cantidad es opcional. Construye los siguientes métodos para la clase:

● Un constructor, donde los datos pueden estar vacíos.

● Los setters y getters para cada uno de los atributos. El atributo no se puede
modificar directamente, sólo ingresando o retirando dinero.

● mostrar(): Muestra los datos de la cuenta.

● ingresar(cantidad): se ingresa una cantidad a la cuenta, si la cantidad
introducida es negativa, no se hará nada.

● retirar(cantidad): se retira una cantidad a la cuenta. La cuenta puede estar
en números rojos.

class Cuenta():
    
    def __init__(self, titular, cantidad = None):
        
        self.titular = titular
        self._cantidad = cantidad
    
    @property
    def titular(self):
        
        return self._titular
    
    @property
    def cantidad(self):
        
        return self._cantidad
        
    @titular.setter
    def titular(self, titular):
        
        self._titular = titular
        
    def mostrar(self):
        
        return "Cuenta \n" + "Titular: "+ self.titular.title() + " - Cantidad:" + str(self.cantidad)
       
        
    def ingresar(self, cantidad):
        
        if cantidad > 0:
            
            self._cantidad = self._cantidad + cantidad
        
    def retirar(self,cantidad):
            
        if cantidad > 0:
                
            self._cantidad = self._cantidad - cantidad
            


## Ejercicio 3 (2 puntos)
Vamos a definir ahora una “Cuenta Joven”, para ello vamos a crear una nueva
clase Cuenta Joven que deriva de la anterior. Cuando se crea esta nueva clase,
además del titular y la cantidad se debe guardar una bonificación que estará
expresada en tanto por ciento.Construye los siguientes métodos para la clase:

● Un constructor.

● Los setters y getters para el nuevo atributo.

● En esta ocasión los titulares de este tipo de cuenta tienen que ser mayor de
edad;, por lo tanto hay que crear un método es Titular Válido ( ) que
devuelve verdadero si el titular es mayor de edad pero menor de 25 años y
falso en caso contrario.

● Además la retirada de dinero sólo se podrá hacer si el titular es válido.

● El método mostrar() debe devolver el mensaje de “Cuenta Joven” y la
bonificación de la cuenta.

● Piensa los métodos heredados de la clase madre que hay que reescribir.
class CuentaJoven(Cuenta):
    
    def __init__(self, titular, bonificacion=None, cantidad=None):
        super().__init__(titular,cantidad)
        self.bonificacion = bonificacion
    
    @property
    def bonificacion(self):
        
        return self._bonificacion
    

    @bonificacion.setter
    def bonificacion(self, bonificacion):
        
        self._bonificacion = bonificacion
        
    def mostrar(self):
        
        return "Cuenta Joven\n" + "Titular: "+ str(self.titular) + " - Cantidad:" + str(self.cantidad) + "- Bonificación:"+ str(self.bonificacion)
       
            
    def TitularValido():
        
            return self.titular 

