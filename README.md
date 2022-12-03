# Recursos para JavaScript
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTab05l3ndGtZqyqxgTeOkmB7g2eDGyYrQp60gRu108tIEXOLQTl8tf9Jpx90UiNJEIv1Q&usqp=CAU)
## Tipos de datos
### String - Cadena o secuencia de caracteres
"Hello World" 'Hello World' (Hay que definir cuando usar uno u otro)
### Number - Enteros o decimales
10000 2.8 -9.73 (No deben llevar comillas de lo contrario se tomaran como texto por el compilador)
### Boolean - Los datos boleanos nos dicen si la condicion se cumple o no
true, false
### array: Item list o String list
['tacos','Especiales','Bebidas','Postres'] [5,2,2,3] ['$25','$150','$50','$50'] [true,false,true,false]
### Object - Conformado por Clave (propiedad) y Valor
{ "username"= true "username write"= 'Miriam' "Tacos"= 'Pastor' "¿Cuantos tacos?"= 5 "sale"= true }

## Ruta Alura programación 1
### JavaScript
    <script>
	
        alert("Este es un pop-up en JavaScript");
		
    </script>

Para leer el texto de HTML dentro de JS:
```javascript
        <script>
		
            document.write("La edad de Gonz es...")
            document.write("<br>")
            document.write("?:D")
			
        </script>
```
Para realizar operaciones quitaremos las comillas a los numeros:
```javascript
    document.write("La edad de Gonz es")
    document.write("<br>")
    document.write(2022-1988)
```
Resultado
La edad de Gonz es
34

Para realizar un promedio:
```javascript
    document.write("¿Cual es el promedio de edad de Packo, Bofo y Gonz")
    document.write("Si Gonz tiene 34")
    document.write("Packo tiene 32")
    document.write(" y Boffo 38")
    document.write("<br>")
    document.write(34+32+38/3)
```
Resultado erroneo:
¿Cual es el promedio de edad de Packo, Bofo y Gonz
Packo tiene 32
Si Gonz tiene 34
y Boffo 38
78.66666666666667 //No es el resultado correcto:

Este codigo contiene un error, por que los programas comienzan a resolver por gerarquía, primero la división, despues la multiplicación, la suma y por ultimo la resta. Ademas, aun nos falta un parentesis adicional a los de la función:
```javascript
    document.write("¿Cual es el promedio de edad de Packo, Bofo y Gonz")
    document.write("<br>")
    document.write("Packo tiene 32")
    document.write("<br>")
    document.write("Si Gonz tiene 34")
    document.write("<br>")
    document.write(" y Boffo 38")
    document.write("<br>")
    document.write((34+32+38)/3) //Aquí se realizo el cambio
```
Resultado
¿Cual es el promedio de edad de Packo, Bofo y Gonz
Packo tiene 32
Si Gonz tiene 34
y Boffo 38
34.666666666666664

Para realizar concatenación:
```javascript
document.write("La suma de las edades de Packo, Gonz y Boffo es:...<br>" + (32+34+38));
```
Resultado
La suma de las edades de Packo, gonz y Boffo es:...
104
```javascript
    document.write("Packo nacio en...")
    document.write("<br>");
    document.write(2022-32)
    document.write("<br>");
    document.write("<br>");
    document.write("Gonz nacio en...")
    document.write("<br>");
    document.write(2022-34)
    document.write("<br>");
    document.write("<br>");
    document.write("Boffo nacio en...")
    document.write("<br>");
    document.write(2022-38)
    document.write("<br>");
    document.write("<br>");
```
Resultado
Packo nacio en...
1990

Gonz nacio en...
1988

Boffo nacio en...
1984

Siguiendo la convención hay que seguir las siguientes recomendaciones: ***Respetar la indentación y dejar un espacio de separación entre las etiquetas de Script y nuestro codigo***

## Ahora ¿Cuantos años tiene cada uno?
```javascript
alert("Este mensaje ahora quiere saber ¿Cuantos años tiene cada uno?");
    document.write("<br>");
    document.write("<br>");
    document.write("<h2>¿Cuantos años tiene cada uno?</h2>");
    document.write("Packo tiene: " + (2022-1990) + "años");
    document.write("<br>");
    document.write("<br>");
    document.write("Gonz tiene: " + (2022-1988) + "años");
    document.write("<br>");
    document.write("<br>");
    document.write("Boffo tiene: " + (2022-1984) + "años");
    document.write("<br>");
    document.write("<br>");
```
### Resultado
¿Cuantos años tiene cada uno?
Packo tiene: 32años

Gonz tiene: 34años

Boffo tiene: 38años

## Ahora comencemos con las variables

Definimos a una variable con la palabra** var** y por convención la colocaremos al inicio del programa, despues de esto podemos darle otros usos.


Caso de uso:
Suponiendo que las edades de Packo, Gonz y Boffo quieren ser revisadas en unos años y quiza saber cual era la edad de cada uno de ellos en otro tiempo para esto vamos a definir una variable.

Vamos a revisar cuantos años tenia cada uno en el año 2015, asi cambiamos el año de consulta actual (2022) por la variable year:

### Codigo inicial
```javascript
    document.write("<h2>¿Cuantos años tiene cada uno?</h2>");
    document.write("Packo tiene: " + (2022-1990) + "años");
    document.write("<br>");
    document.write("<br>");
    document.write("Gonz tiene: " + (2022-1988) + "años");
    document.write("<br>");
    document.write("<br>");
    document.write("Boffo tiene: " + (2022-1984) + "años");
    document.write("<br>");
    document.write("<br>");
```
### Resultado
Packo tiene: 32años

Gonz tiene: 34años

Boffo tiene: 38años

### Sustituyendo por la variable:
```javascript

    var year = 2015

    document.write("<h2>¿Cuantos años tenia cada uno en el 2015?</h2>");
    document.write("Packo tenia: " + (year-1990) + "años");
    document.write("<br>");
    document.write("<br>");
    document.write("Gonz tenia: " + (year-1988) + "años");
    document.write("<br>");
    document.write("<br>");

    year = 2010

    document.write("Boffo tenia: " + (year-1984) + "años");
    document.write("<br>");
    document.write("<br>");
```
### Resultado
Packo tenia: 25años

Gonz tenia: 27años

Boffo tenia: 26años

Pero hay algo extraño, la edad de boffo no es congruente. Esto se debe a que la variable se cambio de **2015** a **2010** dando otro cálculo, por lo tanto otro caso de uso.

### Nota
Si se re-atribuye la **var ** con un valor diferente entonces solo tenemos que escribir el **valor** ya que al inicio declaramos la variable.


####  Ahora vamos a definir el promedio de las edades de Jimena, Karla y Karely
Las edades son:
```javascript
document.write("Jimena tiene: " + (2022-1995));
    document.write("<br>");
    document.write("Karla tiene: " + (2022-1990));
    document.write("<br>");
    document.write("Karely tiene: " + (2022-1985));
```
#### Resultado
Jimena tiene: 27
Karla tiene: 32
Karely tiene: 37

Ahora ¿Cúal es el promedio de las edades de Jimena, karla y Karely?
```javascript
var edadJimena = 27;
    var edadKarla = 32;
    var edadKarely = 37;

    var nombre1 = "Jimena"
    var nombre2 = "Karla"
    var nombre3 = "Karely"

    //Como es la primera vez que se utilizan las variables para definir las edades de cada una, entonces debemos agregar la palabra var al inicio de la variable

    //promedio = (27+32+37)/3 seria lo correcto pero ahora vamos a sustituir los numeros por las nuevas variables ya declaradas para saber; que tal edad pertenece a cada mujer, variable anterior "promedio = (27+32+37)/3" y seguiremos generando el mismo resultado.

    promedio = (edadJimena + edadKarla + edadKarely)/3;

    document.write("El promedio de las edades de " + nombre1 + " , " + nombre2 + " y " + nombre3 + " es: " + Math.round(promedio));
    document.write("<br>");
    document.write("<br>");
    document.write("Notamos que en los casos anteriores la respuesta contenia decimales y en este caso es un número entero, esto paso por que agregamos la función Math.round que redondea los numeros hacia arriba")
    //Tambien podemos atribuirle texto a las variables no solo numeros, ahora veremos el codigo completo concatenado

```
#### Resultado
El promedio de las edades de Jimena , Karla y Karely es: 32

Notamos que en los casos anteriores la respuesta contenia decimales y en este caso es un número entero, esto paso por que agregamos la función "Math.round" sin comillas que redondea los numeros hacia arriba.

## Ejercicio
```javascript
document.write("5 por 1 es " + 5 * 1 + "<br>");
    document.write("5 por 2 es " + 5 * 2 + "<br>");
    document.write("5 por 3 es " + 5 * 3 + "<br>");
    document.write("5 por 4 es " + 5 * 4 + "<br>");
    document.write("5 por 5 es " + 5 * 5 + "<br>");
    document.write("5 por 6 es " + 5 * 6 + "<br>");
    document.write("5 por 7 es " + 5 * 7 + "<br>");
    document.write("5 por 8 es " + 5 * 8 + "<br>");
    document.write("5 por 9 es " + 5 * 9 + "<br>");
    document.write("5 por 10 es " + 5 * 10 + "<br>");
```
```html
<p>
5 por 1 es 5
5 por 2 es 10
5 por 3 es 15
5 por 4 es 20
5 por 5 es 25
5 por 6 es 30
5 por 7 es 35
5 por 8 es 40
5 por 9 es 45
5 por 10 es 50
</p>
```

¿Si queremos la tabla de 8? Tenemos que hacer la alteración de los valores en diferentes lugares. ¿Qué podemos hacer para calcular la tabla de multiplicar de otros números sin necesidad de realizar tantas alteraciones?

#### Entonces:
```javascript
var number = 8

    document.write("5 por 1 es " + number * 1 + "<br>");
    document.write("5 por 2 es " + number * 2 + "<br>");
    document.write("5 por 3 es " + number * 3 + "<br>");
    document.write("5 por 4 es " + number * 4 + "<br>");
    document.write("5 por 5 es " + number * 5 + "<br>");
    document.write("5 por 6 es " + number * 6 + "<br>");
    document.write("5 por 7 es " + number * 7 + "<br>");
    document.write("5 por 8 es " + number * 8 + "<br>");
    document.write("5 por 9 es " + number * 9 + "<br>");
    document.write("5 por 10 es " + number * 10 + "<br>");
```
Para obtener el resultado de multiplicar los numeros por 8 declaramos: var number = 8

```html
<p>
5 por 1 es 8
5 por 2 es 16
5 por 3 es 24
5 por 4 es 32
5 por 5 es 40
5 por 6 es 48
5 por 7 es 56
5 por 8 es 64
5 por 9 es 72
5 por 10 es 80
</p>
```

El resultado es correcto pero nuestro texto no, entonces hay que definir tambien una variable para el texto: var valor = 8

```javascript
var valor = 8

    document.write(valor  + " por 1 es " + number * 1 + "<br>");
    document.write(valor  + " por 2 es " + number * 2 + "<br>");
    document.write(valor  + " por 3 es " + number * 3 + "<br>");
    document.write(valor  + " por 4 es " + number * 4 + "<br>");
    document.write(valor  + " por 5 es " + number * 5 + "<br>");
    document.write(valor  + " por 6 es " + number * 6 + "<br>");
    document.write(valor  + " por 7 es " + number * 7 + "<br>");
    document.write(valor  + " por 8 es " + number * 8 + "<br>");
    document.write(valor  + " por 9 es " + number * 9 + "<br>");
    document.write(valor  + " por 10 es " + number * 10 + "<br>");
```
#### Resultado

```html
<p>
8 por 1 es 8
8 por 2 es 16
8 por 3 es 24
8 por 4 es 32
8 por 5 es 40
8 por 6 es 48
8 por 7 es 56
8 por 8 es 64
8 por 9 es 72
8 por 10 es 80
</p>
```
![](https://img.shields.io/github/followers/GonzaloAqui?style=social)![](https://img.shields.io/github/watchers/GonzaloAqui/LaunchX-LATAM22?style=social)
