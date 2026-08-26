# Trabajo Práctico Final
**Importante** La fecha de entrega es el 15/11/2021 ya que las actas se cargan en el Guaraní el 19/11.

Agreguen al principio del archivo un comentario del tipo:

```C
/*************************
 * Ingenieria en Computación - UNRN Andina
 * Programación 1
 * minombredeusuario de GitHub
 *************************/
```

La evaluación de los items del trabajo tendrán en cuenta los siguientes aspectos:

1. Prolijidad
2. Uso de funciones
3. Uso de memoria dinámica (`malloc`)
4. Reducción al mínimo de duplicación de datos.

# Ejercicio 1 - Cinta de calculo

Implementar las funciones y el programa que permitan la realización de cálculos simples a partir de instrucciones tomadas de un archivo de texto.

El objetivo es tomar del archivo los valores y la operación que debe ser aplicada, como una calculadora de contador.

El símbolo `=` debe ser usado para obtener un resultado y desconectar las operaciones siguientes.

### Operadores mínimos aceptados

Idealmente, las operaciones aritméticas deben de estar implementadas en funciones.

* suma (`+`)
* resta (`-`)
* promedio (a)
* multiplicación (`*`)
* resultado (`=`)

**Ejemplo de entrada**

```
1
2
3
+
5
-
=====
10
11
+
=====
```

El resultado esperado es mostrar por pantalla los cálculos que se hacen, los mismos van apilando los resultados anteriores.

**Ejemplo de salida**

```
1 + 2 + 3 + 6 - 5 = 1
10 + 11 = 21
```

*Este formato de salida es solo un ejemplo y pueden desarrollar uno propio.*

### Consideraciones generales

* Los números contenidos en el archivo serán de tipo ℤ y estarán comprendidos en el rango (-2^16 < valor < 2^16). Si no lo están se deberá rechazar la entrada.
* Múltiples operadores iguales deben ser tomados como uno solo, de forma que puedan ser usados en el archivo como separador.
* Si la linea contiene múltiples operadores diferentes, deben indicar que hay un error en la entrada.
* Pueden usar las funciones de String seguro del TP5 (como librería) así como las funciones de procesamiento y conversión de datos presentes en la Standard Library.
* Pueden usar el ejemplo `argumentos.c` del repositorio [INGCOM-UNRN-P1/ejemplo-c/clasenueve](https://github.com/INGCOM-UNRN-P1/ejemplo-c/tree/main/clasenueve) para pasar el nombre del archivo.

# Ejercicio 2 - Buscaminas

El venerable Buscaminas es un juego en el que tenemos que encontrar los explosivos ocultos en una grilla.

La búsqueda se completa con la indicación de cuantas minas hay adyacentes a una celda:

```
╔════╦════╦════╦════╦════╦════╗
║ -- ║ C0 ║ C1 ║ C2 ║ C3 ║ C4 ║
╠════╬════╬════╬════╬════╬════╣
║ F0 ║ 0  ║ 0  ║ 0  ║ 0  ║ 0  ║
╠════╬════╬════╬════╬════╬════╣
║ F1 ║ 1  ║ 1  ║ 1  ║ 0  ║ 0  ║
╠════╬════╬════╬════╬════╬════╣
║ F2 ║ 1  ║ M  ║ 2  ║ 1  ║ 1  ║
╠════╬════╬════╬════╬════╬════╣
║ F3 ║ 1  ║ 1  ║ 2  ║ M  ║ 1  ║
╠════╬════╬════╬════╬════╬════╣
║ F4 ║ 0  ║ 0  ║ 1  ║ 1  ║ 1  ║
╚════╩════╩════╩════╩════╩════╝
```

*En Discord les comparto una planilla que da los valores de minas adyacentes esperado para tener algo mas gráfico*

Las celdas indican `0` cuando no hay explosivos cerca, y de ahí hasta `8` que es el peor caso; la celda esta completamente rodeada de minas.

Cada celda puede contener:

* Un explosivo
* El numero de explosivos adyacentes.
* Una celda descubierta por el jugador.
* Una mina marcada por el jugador.

Los archivos deberían de ser legibles con un editor de textos (incluso si esto revela la ubicación de las minas).

## Programa 1

Su trabajo es crear un programa que debe solicitar al usuario las dimensiones del tablero y luego las  coordenadas de las minas que seran usadas para crear el mapa de juego.

Este tablero debe ser guardado en un archivo de texto. No olviden indicar las dimensiones del mismo, la ubicación de las minas y las adjacencias. (No es estrictamente necesario, pero puede ser útil guardar cuantas minas contiene el tablero)

## Programa 2

Para esta parte, se debe crear un programa que cargue el mapa y permita jugar.

El jugador tiene dos acciones disponibles:

1.  Descubrir una celda:
    1. Si la celda esta vacía (`0`), se deben destapar las celdas adjacentes vacias.
    2. Si la celda contenía una mina, el jugador pierde.
2. Marcar una mina
    1. Hay tantos marcadores de minas como explosivos en el campo.
    2. Si el jugador marca correctamente todas las minas, gana el juego.

### Opcionales/extras

* Guardar la partida, de manera ideal sería en un archivo separado al mapa de juego inicial.

* Verificar que el mapa guardado sea consistente, esto es que la información del tablero es consistente con las dimensiones y cantidad de minas contenidas.

    



