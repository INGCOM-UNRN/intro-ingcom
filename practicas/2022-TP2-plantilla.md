# TP Python #2

## Forma de entrega
 * Cada punto debe ser entregado en un archivo independiente
 * El nombre de cada archivo debe ser ser `ejercicio` seguido 
del numero de ejercicio mas `.py` (el primer ejercicio sera entonces 
`ejercicio1.py`
 * Cada punto está dividido en dos partes; la función a implementar y 
 el programa que hace uso de la misma.
 * Toda la parte interactiva con el usuario (input/print) debe estar 
 implementada en la función principal().
 * Cada archivo debe seguir la estructura indicada dentro del archivo 
 plantilla.py, reemplacen con su nombre y nombre de usuario de GitHub.
 * Siguiendo con la plantilla.py; el programa que hace uso de lo que 
 debe residir dentro de la función prueba de forma de que pueda ser 
 ignorado al usarlo como librería. (Al final de este documento copio 
 la plantilla para referencia también)
 * En ningún caso se aceptará el uso de variables globales. Toda la
  información necesaria para el funcionamiento de las funciones a 
  desarrollar tienen que ser pasados como argumentos de las mismas.
 * Utilicen nombres de variables descriptivos siempre.
 * Los archivos del ejercicio deben ir en la carpeta `src` y los 
 tests en `tests`
 * Los nombres y el formato general, deben seguir lo indicado por el PEP8.
 * A diferencia del TP anterior, acá no se provee el prototipo de la 
 función a implementar. Con un criterio similar, creen la función que 
 cumpla con la consigna de manera separada a la que interactuá con el 
 usuario. Si están muy trabados podemos conversar cuál es la manera 
 que puede tener.

## Importante
Muchas de las funciones pedidas ya se encuentran implementadas como parte 
de Python, implementen las funciones sin depender de esta funcionalidad 
integrada, sin embargo, pueden usar esta funcionalidad para verificar 
su funcionamiento. Esto incluye tambíen a los atajos, prefieran utilizar 
lazos indefinidos.

## Ejercicios

### 1. Pares e impares
Escribir una función que retorne `True` cuando un número entero es par 
y `False` cuando no lo sea, sin utilizar módulo. (`%`)

### 2. Estadísticas
Implementar una función que obtenga los máximos, mínimos y promedio de 
una secuencia con números, retornando los valores como una `tuple`.

Sin utilizar lazos `for` o las funciones integradas del lenguaje 
que procesan secuencias.

### 3. Súper-puestos
Desarrollar una función que indique el grado de superposición entre dos listas.
Siendo 0 sin superposición y uno para cada elemento superpuesto.
```python
['H', 'o', 'l', 'a', ' ', 'M', 'u', 'n', 'd', 'o']
```
y 
```python
['H', 'o', 'l', 'a']
```
Tienen una superposición de cuatro elementos.

#### Extra #1
Indicar en lugar de la cantidad de caracteres superpuestos, la posicion 
de inicio de la superposición.

### 4. Fibonacci
La sucesión de Fibonacci es una sucesión infinita donde cada elemento es 
la suma de los dos anteriores. En la misma, los dos primeros términos 
son 1. (En algunos lugares se toma el primer término en 0 y el segundo en 1)
Implementar una función que permita obtener el n-esimo termino de la 
sucesión de Fibonacci. Siendo este número un entero positivo mayor a 2.

### 5. Corchetes balanceados
Implementar una función que determine si una cadena con corchetes 
está balanceada.

Es decir, si cada corchete que abre, tiene su par que cierra. 
El resultado debe ser un valor lógico indicando si esta o no balanceado.

**Ejemplos**
```
   (vacio)      True
   []           True
   [][]         True
   [[][]]       True
   ][           False
   ][][         False
   []][[]       False
```
La funcion deberia de ignorar todo lo que no sean corchetes.

#### Extra #1
Hacer que la funcion reciba _que_ par de simbolos buscar si esta 
balanceado. (como para pasar parentesis, llaves o cualquier otro)

#### Extra #2
Hacer que la función verifique el balanceo simultaneo de parentesis, 
llaves y corchetes.

### 6. El Cifrado del Cesar
El cifrado César o cifrado de rotación usa una encriptación de 
sustitución simple. Esto significa que cada caracter se sustituye 
por otro caracter de acuerdo con un sistema especifico. 

La codificación debe ser tal que la palabra codificada contenga 
unicamente caracteres del tipo AZaz y 0 a 9, de manera que al 
codificar las ultimas letras del abecedario se vuelva a las primeras letras.

**Por ejemplo**, el método conocido y muy utilizado ROT13 rota 
el alfabeto con 13 posiciones, resultando en A->N, B->O... Y->L y Z->M.

* Implementar una funcion que codifique un texto rotandolo 
una cantidad de posiciones ajustable.

* Implementar la funcion que decodifique el texto rotado una 
cantidad de posiciones ajustable.

Una buena forma para verificar este ejercicio es codificar y 
decodificar un texto y compararlo con lo que fué ingresado originalmente.

**Tip**: Implementar las funciones utilizando las funciones `ord` y `chr`.

