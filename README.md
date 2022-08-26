# Test de JavaScript 
--- 
.
## 1️⃣Responde las siguientes preguntas en la sección de comentarios:
### ¿Qué es una variable?
Una variable es un espacio en memoria, es la forma en que le decimos al computador que vamos a guardar un dato de cualquier tipo ([tipos de datos primitivos](https://developer.mozilla.org/es/docs/Glossary/Primitive)) en un lugar de la memoria de nuestro computador. Para declarar una variable en JavaScript usamos las palabras reservadas let y const, estas dos tienen un diferente uso.
 - __let__: Hacemos uso de esta palabra para declarar una variable cuyo valor puede modificarse durante la ejecucion del programa, es decir, el valor que asignamos a las variables declaradas con esta palabra puede variar durante el flujo del progama.
``` let edad = 17```  
 - __const__: Hacemos uso de esta palabra para declarar una constante cuyo valor no podra modificarse durante la ejecucion del programa, podemos almacenar valores constantes.
 - ``` const fullName = 'Héctor Galindo Pedraza' ```
 .
### ¿Cuál es la diferencia entre declarar e inicializar una variable?
Cuando vamos a hacer uso de una variable en nuestros programas podemos declarar la variable para que se cree ese espacio en memoria y luego en otra instruccion del programa la inicializaremos, creamos el espacio en memoria y esta pendiente para que le asignemos un valor. Tambien podemos declarar e inicializar la variable al tiempo.
``` 
    let i     // Declaramos la variable i
    let i = 4 // Inicializamos o asignamos el valor 4 a la variable i
    const PI = 3.1416 // Declaramos e inicializamos la constante PI
```
.
### ¿Cuál es la diferencia entre sumar números y concatenar strings?
Cuando usamos el operador de suma para hacer una operacion entre dos datos de tipo entero, este nos dara el resultado de la suma, ya que los dos datos que usamos son de __tipo entero__.
```
 let num1 = 4
 let num2 = 5
 let suma = num1 + num2 // Suma almacenara el resultado de la operacion que es 9
 
```
Y con este operador de suma tambien podemos concatenar dos datos de tipo string, aunque tambien podemos hacer uso de los __template string__.
```
    let name = 'Héctor'
    let lastName = 'Galindo'
    let fullName = name + lastName
    > fullName => 'HéctorGalindo'
```
FullName almacena la concatenacion de las variables `name` y `lastName`, las cuales almacenan datos de tipo string, por lo que el operador de suma en este caso funciona para concatenar las dos cadenas. Pero si te diste cuenta las dos cadenas no tienen un espacio en medio, esto lo solucionamos concatenando un string con un caracter de espacio en medio de `name` y `lastName`.
```
    let name = 'Héctor'
    let lastName = 'Galindo'
    let fullName = name + " " +  lastName 
    > fullName => 'Héctor Galindo'
```
Pero emplear este metodo puede llegar a confundirnos y ocupar mucho espacio en nuestro código si trabajamos con mas cadenas concatenadas, en cambio podemos hacer uso de los __template strings__.
```
    let name = 'Héctor'
    let lastName = 'Galindo'
    let fullName = `${name} ${lastName}`
    > fullName => 'Héctor Galindo'
```
Y ahora, ¿Qué pasa si concatenamos un dato de tipo entero y uno de tipo string? Veamos.
```
    let numero = 5
    let objetos = 'libros'
    let conct = `${numero} ${objetos}`
    > conct => '5 libros'
```
Como se puede ver la variable `conct` almacena un string con los dos datos concatenados. Pero, ¿Por qué pasa estó si la variable número es de tipo entero? Lo que sucede en este caso se le llama [coercion implicita](https://mauriciogc.medium.com/javascript-ecuaciones-complejas-440578bcfad7).

### ¿Qué operador me permite sumar o concatenar?
El operador de suma "+" funciona para concatenar y sumar, depende de que tipos de datos usemos, ya que si utilizamos este operador con un dato de tipo entero y un dato de tipo string sucedera lo que llamamos coercion implicita.
.
## 2️⃣ Determina el nombre y tipo de dato para almacenar en varibles la siguiente información:
- `Nombre == 'string'`
- `Apellido == 'string'`
- `Nombre de usuario en Platzi == 'string'`
- `edad == 'number'`
- `email == 'string'`
- `mayorDeEdad == 'boolean'`
- `dineroAhorrado == 'number'`
- `deudas == 'number'`
.
## 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior.
```
    const nombre = 'Héctor'
    const apellido = 'Galindo'
    let username = 'hecgph'
    let edad = 17
    let email = 'hec.gph@proton.me'
    let mayorDeEdad = false
    let dineroAhorrado = 100000
    let deudas = 0
```
. 
## 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
```
    const fullName = nombre + apellido
    let dineroReal = dineroAhorrado - deudas
```
.
# Funciones
---
## 1️⃣ Responde las siguientes preguntas:
### ¿Qué es una función?
Una funcion es un bloque de código que cumple con una tarea en especifico, ayuda a reutilizar código y modularizar nuestros programas. Las funciones pueden recibir parametros, que son variables que le pasamos a la hora de mandar a llamar a nuestra funcion, los valores que le pasamos se llaman __argumentos__. Los parametros estáran disponibles dentro de la función, esto por su [scope](https://developer.mozilla.org/es/docs/Glossary/Scope).
__Sintaxis:__
```
    function nombreDeMiFuncion (parametro1, parametro2)
    {
        // Código a ejecutar
    }
    nombreDeMiFuncion(argumento1, argumento2)
```
### ¿Cuándo me sirve usar una función en mi código?
Cuando necesitamos que un bloque de código haga una tarea en especifico y ademas tenga que ejecutarse varias veces cambiando valores en sus variables.
### ¿Cuál es la diferencia entre parámentros y argumentos de una función?
Le llamamos __parametro__ al nombre que ponemos dentro de parentesis a la hora de crear nuestra funcion, y le llamamos __argumentos__ a los valores que le damos a los campos de los argumentos que requiere la funcion para cumplir con su tarea.
.
## 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
En una función 👇
```
    const whoami = (name, lastName, nickName) => {
    const completeName = `${name} ${lastName}`
    console.log(`Mi nombre es ${completeName}, pero prefiero que me digas ${nickName}.`)
}
```
.
# Condicionales
--- 
## 1️⃣ Responde las siguientes preguntas:
### ¿Qué es un condicional?
Un condicional es una estructura de control que nos permite cambiar el flujo de ejecucion del programa evaluando si una expresion es verdadera o falsa.
### ¿Qué tipo de condicionales existen en JavaScript y cuáles son sus diferencias?
Existen dos estructuras de condicionales, estás son: `if...else` y `switch`. Tambien tenemos los operadores lógicos que son: `!`, `&&` y `||` que crean la posibilidad de establecer condiciones`
- `if`: Si la expresion dentro de los parentesis es verdadera se ejecutara el codigo entre las llaves.
    ``` 
    if (expresion)
    {
        // Ejecuta el código si la expresion es verdadera
    }
    ```
- `if ... else`: Si la expresion dentro de los parentesis es verdadera se ejecuta el primerbloque de código, si no se ejecuta el código dentro de las llaves del else.
    ```
        if (expresion)
        {
            // Ejecuta el código si la expresion es verdadera.
        }
        else
        {
            // Ejecuta el código si la expresion es falsa.
        }
    ```
- `else if`: Si la expresion dentro de los parentesis del `if ()` es falsa, entonces pasa a evaluar una seguna condicion.
    ```
        if (expresion)
        {
            // Ejecuta el código si la expresion es verdadera.
        }
        else if (expresion)
        {
            // Ejecuta el código si la primera expresion es falsa y la sengunda verdadera
        }
        else 
        {
            // Ejecutael código si ningua de las condiciones anteriories es verdadera.
        }
    ```
- `switch`:Evalua un valor en diferentes casos con sus respectivas expresiones, si la expresion es verdadera necesitara un `break` para que termine de evaluar los casos, de lo contrario seguira ejecutando la estructura.
    ```
    const mascota = "perro";
 
    switch (mascota) {
      case "lagarto":
        console.log("Tengo un lagarto");
        break;
      case "perro":
        console.log("Tengo un perro");
        break;
      case "gato":
        console.log("Tengo un gato");
        break;
      case "serpiente":
        console.log("Tengo una serpiente");
        break;
      case "loro":
        console.log("Tengo un loro");
        break;
      default:
        console.log("No tengo mascota");
        break;
    } 
    ```
    ### ¿Puedo combinar funciones y condicionales?
    ¡Sí claro! Podemos combinar funciones y condicionales, por ejemplo si necesitamos validar el valor que nos retorna una funcion podemos usar una estructura condicional.
    ## 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
    ```
        const tipoDeSuscripcion = "Basic";

        switch (tipoDeSuscripcion) {
           case "Free":
               console.log("Solo puedes tomar los cursos gratis");
               break;
           case "Basic":
               console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
               break;
           case "Expert":
               console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
               break;
           case "ExpertPlus":
               console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
               break;
        }
    ```
    __If, else if y else__:
    ```
        const tipoDeSuscripcion = 'Basic'

        if (tipoDeSuscripcion == 'Free')
        {
            console.log("Solo puedes tomar los cursos gratis");
        }
        else if (tipoDeSuscripcion == 'Basic')
        {
            console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        }
        else if (tipoDeSuscripcion == 'Expert')
        {
            console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        }
        else if (tipoDeSuscripcion == 'ExpertPlus')
        {
            console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        }
    ```
 
 
 
 
