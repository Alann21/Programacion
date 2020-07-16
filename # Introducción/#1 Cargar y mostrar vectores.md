# Cargar vectores

Insertar valores en un vecor es sencillo, pero si hace falta que el usuario ingrese los valores, es un poquito más complejo.

Cuando queremos que el usuario ingrese valores en un vector, generalmente queremos que ingrese varios números. Por ende, no es muy buena idea colocar un `scanf` por cada valor que queremos ingresar.

En vez de eso, se suelen utilizar ciclos `for`. 

Lo único que hace falta saber es la cantidad de valores que necesitamos ingresar.

Este sería un ejemplo de un programa que lee 5 numeros.

```c++
	#include <stdio.h>

	int main() {
		int vector[5];

		for (int i = 0; i < 5; ++i) {
			scanf("%d", &vector[i]);
		}
	}
```

El programa usa un ciclo for que se repite 5 veces. Comienza con `i` valiendo 0 y cada vez que el ciclo se repite aumenta su valor en 1, hasta llegar a 5. En otras palabras los valores que toma `i` son:

```c++
	0 
	1
	2
	3
	4
```
Y cada vez que toma uno de estos valores se ejecuta esta instrucción:

```c++
	scanf("%d", &vector[ i ]);
```

Lo imporante es que el valor que se ingresa se guarda en la posición `i`. Ya que `i` va a empezar valiendo 0 y va a ir aumentando hasta antes de que llegue a 5.

En otras palabras, lo anterior es lo mismo que colocar:

```c++
	scanf("%d", &vector[ 0 ]);
	scanf("%d", &vector[ 1 ]);
	scanf("%d", &vector[ 2 ]);
	scanf("%d", &vector[ 3 ]);
	scanf("%d", &vector[ 4 ]);
```

<br>


## Mostrar vectores

Si hace falta __mostrar__ un vector, la lógica sería la misma. Sólo que, en vez de pedir valores, habría que imprimirlos en pantalla.

Así como para pedir algo usamos `scanf`, para mostrar algo por pantalla usamos `printf`. Entonces, por lógica, lo que habríá que hacer es reemplazar el `scanf` por un `printf`.

El código que habría que usar para mostrar un valor sería el siguiente:

```c++
	printf("%d", vector[i]);
```

Pero si usamos esto para el programa de antes, el resultado sería algo así como lo siguiente:

```console
1351942
```

O sea, todos los valores se mostrarían pegados. Esto es porque el programa muestra los valores uno después del otro, no los separa de ninguna manera ya que no le indicamos que haga esto. Para evitar que eso ocurra se podría imprimir un espacio o un salto de línea luego de cada valor.

Por ejemplo:

```c++
	printf("%d \n", vector[i]);
```

De esta manera, cada valor iría seguido de un espacio y un salto de línea.

<br>



## Resultado

El código con todo lo anterior junto sería:

```c++
	#include <stdio.h>

	int main(){
		int vector[5];
		
		// Se ingresan los valores.
		for (int i = 0; i < 5; ++i) {
			scanf("%d", &vector[i] );
		}

		// Mensaje, es sólo estético.
		printf("\nLos numeros ingresados son:\n");

		// Se muestran los valores.
		for (int i = 0; i < 5; ++i) {
			printf("%d \n", vector[i] );
		}
	}
```

<br>



> ###### __Nota:__
> Intenten no utilizar el nombre "vector" ya que en C++ es el nombre de una instrucción. Probablemente no van a tener problemas pero puede ser molesto en algunos editores de código ya que se confunden entre sí.\
> Siempre es mejor usar nombres cortos según la función que vaya a tener, como _"notas"_. Si no tiene una función clara, puede ser _"vect"_ o una letra.