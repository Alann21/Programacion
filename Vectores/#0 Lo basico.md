# Introducción a los vectores

Un vector es un conjunto de números, ajá, pero el motivo por el cual se usan vectores en lugar de muchas variables sueltas es para poder utilizar estos números fácilmente.

Si quisieras guardar un valor en una variable, sería tan simple como escribir algo así:

```C++
	scanf("%d", &variable);
```

Pero si quisieras guardar 10 valores, tendías que repetir eso 10 veces. Lo cual sería una perdida de tiempo y de espacio.

Con vectores, es como si tuvieras estas 10 variables pero todas se llaman igual. Digamos que se llaman `a`. Esto sirve para que si queremos guardar 10 valores, podamos hacerlo guardándolos en `a`, la cual no es una sóla variable, sino muchas con el mismo nombre (digamos).

Ahora tenemos un problema, ¿Cómo se pueden distinguir los distintos valores? Es decir, normalmente podríamos decir que ` a = 4 `, entonces el valor de 'a' es 4, pero entonces sólo podríamos guardar un sólo valor. Para esto, se usa el _indice_. Este es un número que se coloca entre corchetes e indíca el valor que queremos usar. O sea, cada número indica un valor distinto, como si fuera el nombre de la varible. Los 'valores' de un vector se suelen llamar _Posiciones_

Por ejemplo, si queremos guardar los valores 5, 7 y 4, podríamos escribir algo como:

```c++
	
	int a = { 5, 7, 4 }

```
De esta dorma 'a' contendría en cada posición los números 5, 7 y 4, guardados en la primera, segunda y tercera posición.

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

> * Estos ejemplos son sólo conceptuales
