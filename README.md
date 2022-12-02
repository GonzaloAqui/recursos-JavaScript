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

    var year=2010

    document.write("Boffo tenia: " + (year-1984) + "años");
    document.write("<br>");
    document.write("<br>");
```
### Resultado
Packo tenia: 25años

Gonz tenia: 27años

Boffo tenia: 26años

Pero hay algo extraño, la edad de boffo no es congruente. Esto se debe a que la variable se cambio de **2015** a **2010** dando otro cálculo, por lo tanto otro caso de uso.


![](https://img.shields.io/github/followers/GonzaloAqui?style=social)![](https://img.shields.io/github/watchers/GonzaloAqui/LaunchX-LATAM22?style=social)
