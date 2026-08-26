# TP5-plantilla Python

## Forma de entrega
* Cada punto debe ser entregado en un archivo independiente

* El nombre de cada archivo debe ser ser `tp5ej` seguido del numero de ejercicio mas `.py` (el primer ejercicio sera entonces `tp5ej1.py`

* Cada punto esta dividido en dos partes; la función a implementar y el programa que hace uso de la misma.

* Toda la parte interactiva con el usuario (`input`/`print`) debe estar implementadada en la función `prueba()`.

* Cada archivo debe seguir la estructura indicada dentro del archivo `plantilla.py`, reemplacen con su nombre y nombre de usuario de GitHub. 

* Siguiendo con la `plantilla.py`; el programa que hace uso de lo que  debe residir dentro de la función `prueba` de forma de que pueda ser ignorado al usarlo como libreria. (Al final de este documento copio la plantilla para referencia tambien)

* En ningún caso se aceptara el uso de variables globales. Toda la información necesaria para el funcionamiento de las funciones a desarrollar tienen que ser pasados como argumentos de las mismas.

* A diferencia del TP anterior, acá no se provee el prototipo de la funcion a implementar. Con un criterio similar, creen la funcion que cumpla con la consigna de manera separada a la que interactua con el usuario. Si estan muy trabados podemos conversar cual es la forma que puede tener.

* Usen nombres de variables descriptivos siempre.

* Los nombres y el formato general, deben seguir lo indicado por el PEP8.

## Importante
Muchas de las funciones pedidas ya se encuentran implementadas como parte de Python, implementen las funciones sin depender de esta funcionalidad integrada, sin embargo, pueden usar esta funcionalidad para verificar su funcionamiento. Esto incluye tambíen a los atajos, usen lazos.

### 1. Pares e impares
Escribir una función que retorne `True` cuando un número entero es par y `False` cuando no lo sea, sin utilizar módulo. (`%`)

### 2. Fibonacci
La sucesión de Fibonacci es una sucesión infinita donde cada elemento es la suma de los dos anteriores. En la misma, los dos primeros términos son 1. (En algunos lugares se toma el primer termino en 0 y el segundo en 1)

Implementar una funcion que permita obtener el n-esimo termino de la sucesión de Fibonacci. Siendo este número un entero positivo mayor a 2.

[Fibonacci - OEIS](http://oeis.org/A000045)


### 3. ¡Tribonacci!
La secuencia de Tribonacci es el mismo concepto que la de Fibonacci común, pero acá en lugar de sumar dos terminos; se suman de a tres. [Tribonacci - OEIS](http://oeis.org/A000213) 

Los tres primeros terminos son uno y el termino 4 es la suma de los tres anteriores.

Implementar una funcion que permita obtener el n-esimo termino de la suceción Tribonacci, siendo este termino un numero entero positivo mayor a 3.

### 4. Números perfectos
“Un numero entero es llamado perfecto cuando este numero es igual a la suma de sus divisores exactos”

Escribir una función que determine si un numero entero positivo es un número perfecto.

### 5. Inversión de mayusculas
Implementar una funcion que dada un texto, deje en minuscula lo que esté en mayuscula y en mayuscula lo que esté en minuscula.

**Ejemplo**:  `Hola Mundo!` -> `hOLA mUNDO!`

### 6. Parentesis balanceados
Implementar una función que determine si **una** cadena con parentesis está balanceada.

Es decir, si cada parentesis que abre, tiene su par que cierra.
El resultado debe ser un valor lógico indicando si esta o no balanceado.

**Ejemplos**
```
   (vacio)      OK
   []           OK   
   [][]         OK   
   [[][]]       OK 
   ][           NO OK
   ][][         NO OK
   []][[]       NO OK
```
La funcion deberia de ignorar todo lo que no sean parentesis.

**Extra**: Permitir la modificacion de los caracteres a parentesis, llaves, o cualquier otro par de caracteres.

### 7. Distancias
Escriba una funcion que determine la distancia entre dos números.

Implementar este ejercicio sin utilizar la función valor absoluto `abs()`.

**Ejemplo** La distancia entre -6.5 y 6.0 es 12.5

### 8. El Cifrado del Cesar
El cifrado César o cifrado de rotación usa una encriptación de sustitución simple. Esto significa que cada caracter se sustituye por otro caracter de acuerdo con un sistema especifico. 

La codificación debe ser tal que la palabra codificada contenga unicamente caracteres del tipo AZaz y 0 a 9, de manera que al codificar las ultimas letras del abecedario se vuelva a las primeras letras.

**Por ejemplo**, el método conocido y muy utilizado ROT13 rota el alfabeto con 13 posiciones, resultando en A->N, B->O... Y->L y Z->M.

* Implementar una funcion que codifique un texto rotandolo una cantidad de posiciones ajustable.

* Implementar la funcion que decodifique el texto rotado una cantidad de posiciones ajustable.

Una buena forma para verificar este ejercicio es codificar y decodificar un texto y compararlo con lo que fué ingresado originalmente.

**Tip**: Implementar las funciones utilizando las funciones `ord` y `chr`.


### 9. Factoriones
Un factorión es un número natural que es igual a la suma de los factoriales de sus dígitos.

Implementar una funcion que retorne una lista con todos los factoriones menores a `1.499.999`. [Factorions - OEIS](https://oeis.org/A014080)

**Ejemplo**  `1! + 4! + 5!   =   1 + 24 + 120   =   145 `

Para acelerar la resolución de este problema, pueden implementar una funcion que retorne la lista de factoriales y permitir que la funcion encargada de hacer la busqueda reciba esta lista.

### 10. Texto binario
Implementar una funcion que dado un numero entero positivo, retorne una cadena de texto con su representación binaria.
Implementar una funcion que haga el proceso inverso; dada una cadena de texto, retorne el numero entero.


### 11. Promedio móvil
Un promedio móvil es una media no ponderada de una cantidad menor al total de un conjunto de valores en una serie de datos. Es una forma de controlar variaciones fuertes en la misma. Esta técnica permite ajustar el nivel de suavizado cambiando la cantidad de valores contiguos de la serie que entran en el calculo.

Implementar una función que obtenga una lista con el promedio móvil de otra lista con números enteros. Esta función debe permitir ajustar la cantidad de valores a tomar en cada promedio.

### 12. Comparación de listas
Escribir una función que que determine retornando True si un par de listas contienen los mismos elementos que pueden estar estén ubicados en diferentes posiciones.

### 13. Búsqueda de palabras
Escribir una función que dado un texto y una palabra, retorne la ubicación de la palabra en el texto o una excepción si la palabra no forma parte del texto.

Considerar solo la primera vez que aparezca la palabra a buscar.

### 14. Números capicúa
Escribir una función que determine si un numero entero positivo es capicúa.
