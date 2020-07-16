
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
