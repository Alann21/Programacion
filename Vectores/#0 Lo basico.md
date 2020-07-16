# Introducción a los vectores

Un vector es un conjunto de números, ajá, pero el motivo por el cual se usan vectores en lugar de muchas variables sueltas es para poder utilizar estos números fácilmente.

Si quisieras guardar un valor en una variable, sería tan simple como escribir algo así:

```C++
	scanf("%d", &variable);
```

Pero si quisieras guardar 10 valores, tendías que repetir eso 10 veces. Lo cual sería una perdida de tiempo y de espacio.

Con vectores, es como si tuvieras estas 10 variables pero todas se llaman igual. Digamos que se llaman `a`. Esto sirve para que si queremos guardar 10 valores, podamos hacerlo guardándolos en `a`, la cual no es una sóla variable, sino muchas con el mismo nombre (digamos).

Ahora tenemos un problema, ¿Cómo se pueden distinguir los distintos valores? Es decir, normalmente podríamos decir que ` a = 4 `, entonces el valor de `a` es 4, pero entonces sólo podríamos guardar un sólo valor. Para esto, se usa el _indice_. Este es un número que se coloca entre corchetes e indíca el valor que queremos usar. O sea, cada número indica un valor distinto, como si fuera el nombre de la varible. Los 'valores' de un vector se suelen llamar _Posiciones_

Por ejemplo, si queremos guardar los valores 5, 7 y 4, podríamos escribir algo como:

```c++
	a = { 5, 7, 4 }
```
De esta forma `a` contendría en cada posición los números 5, 7 y 4, guardados en la primera, segunda y tercera posición.

## No entendí

Es como si quisieramos guardar una palabra en una variable. Las variables almacenan sólo valores sueltos. Una palabra contiene varios valores, cada letra es un valor.
Si quisieramos guardar la palabra "Hola", tendríamos que guardar las letras 'H', 'o', 'l', y 'a' como diferentes valores. Usar variables sería un lio y peor aún si queremos guardar varias palabras o una frase.

De la misma forma que podemos guardar varios números juntos, en C también podemos guardar varias letras juntas (lo que suena más logico).

Por lo que si queremos guardar "hola" en una variable podríamos hacer:


```c++
	a = "Hola"
```

Pero en escencia es lo mismo que hacer:

```c++
	a = { 'H', 'o', 'l', 'a' }
```

<br>

>  __Estos ejemplos son sólo conceptuales__

<br>

## Declarar Vectores

Los vectores se declaran como las variables, se coloca el tipo de valor y luego el nombre. La diferencia es que hace falta agregar corchetes para indicarle la cantidad de valores que va a tener:

```c++
	int vector[4];			// un vector de 4 valores
```

y si queremos asignarle los valores desde un inicio no se utilizan corchetes sino llaves luego de un símbolo igual:

```c++
	int vector = { 4, 6, 3, 8 }; 	// un vector con los valores 4, 6, 3 y 8 
```






> ###### __Cuidado__
> No se pueden asignar varios valores a un vector después de crearlo (declararlo). \
> __Este código no funciona:__
>```c++
>	int vector[4];
>	vector = { 4, 6, 3 ,8 };
>```



# Índice
Algo importante a resaltar es que el índice comienza desde 0, no desde 1. O sea que el __primer valor está en la posición 0__. Esto puede sonar confuso al principio, pero en la informática es bastante común comenzar a contar desde 0.

Esto es importante ya que si creamos un vector con x cantidad de valores, cada valor va a estar un lugar antes de donde "debería" estar. Es decir, la primera posición es la 0, la segunda es la 1, la tercera es la 2 y así. 

```c++
	int vector = { 1, 2, 3, 4, 5};
		       ^  ^  ^  ^  ^
	Posición:      0  1  2  3  4
```
