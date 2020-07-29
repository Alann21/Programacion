# Ejercicio 6 (Tp 2)

> "Realizar un programa que lea 2 listas: A y B de N elementos cada una. Mostrar ambas listas y además una lista C, en la cual se asignaron los valores que tiene en común las lista A y B"

## Por partes:

> _que lea 2 listas_

okey, de primeras necesitamos dos listas y hay que __leer__ valores para ingresarlos a cada una.

> _de N elementos cada una_

Cuando dice N está hablando de un número 'x'. Nosotros no podemos deir cuál es ese número, lo tenemos que preguntar.

> _mostrar ambas listas_

Hay que mostrar los valores de cada una.

> _y además una lista C_

Otra lista.

> _en la cual se asignaron los valores que tiene en común las lista A y B_

Bien, hay que sacar los valores en comun de las dos primeras listas para introducirlos en la lista C.

<br>



## Algoritmo

Entonces, de forma lógica, los pasos a seguir serían:

* Preguntar la cantidad de elementos de las listas
    > Es lo primero que hay que hacer porque hay que saber cuantos númumeros pedir.
* Introducir la lista 'A'
* Introducir la lista 'B'
* Guardar los valores en común en C (si hay)
* Mostrar la lista 'A'
* Mostrar la lista 'B'
* Mostrar la lista 'C'

<br>



# En código

Lo primero, la cantidad de elementos. Fácil, es literalmente preguntar un número.

Para ingresar un número usaríamos:

```c++
scanf("%d");        // permite ingresar numeros enteros.
```

<br>


Pero claro, hace falta mostrar algún mensaje en pantalla y además hay que guardar el valor en algún lado, en este caso el enunciado dice que el valor tiene que ser 'n'.

Podríamos hacer algo como:

```c++
printf("Ingrese la cantidad de valores de las listas\n");
scanf("%d", &n);    // Los numeros se guardan en 'n'.
```

<br>


Ahora hay que introducir los valores de la primer lista. Para cargar valores en un vector deberíamos usar un for, y la cantidad de valores que hay que ingresar es igual a `n` (donde está el valor que ingresó el usuario).

Entonces habría que hacer algo como:

```c++
for (i = 0; i < n; ++i) {
    scanf("%d");    // Código que se va a repetir.
}
```

<br>

Y, de nuevo, falta un mensaje para que el usuario sepa qué hacer y hay que guardar el númeor ingresado.

```c++
printf("Ingrese los valores de la lista A\n");
for (i = 0; i < n; ++i) {       // I va a ir desde 0 hasta llegar a 'n'.
    scanf("%d", &a[ i ]);       // Los valores se guardan en 'a' en la posición que vaya tomando i.
}
```

<br>

Ahora sólo repetimos lo mismo pero para la lista 'b'.

```c++
printf("Ingrese los valores de la lista B\n");
for (i = 0; i < n; ++i) {
    scanf("%d", &b[ i ]);
}
```

<br>


Ahora necesitamos obtener los valores en común.

