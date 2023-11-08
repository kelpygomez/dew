# DEWC01: Uso de JavaScript
### Kelpy Gómez Camín | 2 - DAM - DEW

#### Ejercicio 1. Realizar una pequeña aplicación en JavaScript  que muestre lo siguiente
##### -  Utilizar tres tipos distintos de bucles que hay en JavaScript (para cada número un tipo de bucle diferente).:

- Tabla de multiplicar del 7: <b style="color:coral">utilizando for</b>

*Primero creamos un div con una lista a la
que vayamos añadiendo elementos en un documento .html:*
```
<div>
<h3>Tabla de multiplicar del 7:</h3>
<ul id="tablaMultiplicar7"></ul>
</div>
```
*Después creamos la porción del script
correspondiente a esta tabla:*
```
for (let i = 1; i <= 10; i++) {
const resultado = 7 * i;
const item = document.createElement("li");
item.textContent = `7 x ${i} =
${resultado}`;
tablaMultiplicar7.appendChild(item);
} //Añadimos el elemento a la lista como ‘li’.
```
- Tabla de sumar del 8: <b style="color:coral">utilizando while</b>

*Primero creamos un div con una lista a la
que vayamos añadiendo elementos:*
```
<div>
<h3>Tabla de sumar del 8:</h3>
<ul id="tablaSumar8"></ul>
</div>
```
*Después creamos la porción del script
correspondiente a esta tabla:*
```
let num = 1;
while (num <= 10) {
const resultado = 8 + num;
const item = document.createElement("li");
item.textContent = `8 + ${num} =
${resultado}`;
tablaSumar8.appendChild(item);
num++;
}
```
- Tabla de dividir del 9: <b style="color:coral">utilizando do while</b>

*Primero creamos un div con una lista a la
que vayamos añadiendo elementos:*
```
<div>
<h3>Tabla de dividir del 9:</h3>
<ul id="tablaDividir9"></ul>
</div>
```

*Después creamos la poción del script correspondiente a esta tabla:*
```
let divisor = 1;
do {
const resultado = 9 / divisor;
const item = document.createElement("li");
item.textContent = `9 / ${divisor} =
${resultado}`;
tablaDividir9.appendChild(item);
divisor++;
} while (divisor <= 10);
```

#### Ejercicio 2. Sabiendo que cuando desplazamos 1 bit a la derecha dividimos un entero por 2 y cuando lo desplazamos a la izquierda estamos multiplicando por 2; configurar tu web para que también imprima el resultado de las siguientes operaciones empleando desplazamiento de bits:

*Primero, creamos un elemento <'div'> que contenga cada
operación:*
```
<div>
<h3>Operaciones con Desplazamiento de Bits</h3>
<div>
<p id="divisionResult"></p>
</div>
<div>
<p id="multiplicationResult"></p>
</div>
<div>
<p id="divisionResult2"></p>
</div>
<div>
<p id="multiplicationResult2"></p>
</div>
</div>
```
*Y después hacemos que un script las resuelva y muestre el resultado:*
```
<script>
const divisionResult = 125 >> 3;
const multiplicationResult = 40 << 2;
const divisionResult2 = 25 >> 1;
const multiplicationResult2 = 10 << 4;

const divisionResultElement = document.getElementById("divisionResult");
divisionResultElement.textContent = `125 / 8 = ${divisionResult}`;

const multiplicationResultElement = document.getElementById("multiplicationResult");
multiplicationResultElement.textContent = `40 x 4 =
${multiplicationResult}`;

const divisionResult2Element =
document.getElementById("divisionResult2");
divisionResult2Element.textContent = `25 / 2 =
${divisionResult2}`;

const multiplicationResult2Element =
document.getElementById("multiplicationResult2");
multiplicationResult2Element.textContent = `10 x 16
= ${multiplicationResult2}`;
</script>

```
#### Ejercicio 3. A partir del código dado, se pide:
#### - Modificar el código proporcionado para agregar condicionales if que manejen las operaciones matemáticas según el botón que se presione.
```
<script>
function realizarOperacion(operador) {
// Obtener los valores de los números ingresados
var numero1 =
parseFloat(document.getElementById("numero1").value);
var numero2 =
parseFloat(document.getElementById("numero2").value);
// Realizar la operación correspondiente según
el operador
if (operador === '+') {
var resultado = (numero1 +
numero2).toFixed(2);
} else if (operador === '-') {
var resultado = (numero1 -
numero2).toFixed(2);
} else if (operador === '*') {
    var resultado = (numero1 *
numero2).toFixed(2);
} else if (operador === '/') {
var resultado = (numero1 /
numero2).toFixed(2);
}
// Mostrar el resultado en la caja de texto
document.getElementById("resultado").value =
resultado;
}
</script>
```

#### - Modificar el código para usar un condicional switch en lugar de múltiples if para manejar las operaciones matemáticas.
```
<script>
function realizarOperacion(operador) {
// Obtener los valores de los números ingresados
var numero1 =
parseFloat(document.getElementById("numero1").value);
var numero2 =
parseFloat(document.getElementById("numero2").value);
// Realizar la operación correspondiente según
el operador utilizando switch
switch (operador) {
case '+':
var resultado = (numero1 +
numero2).toFixed(2);
break;
case '-':
var resultado = (numero1 -
numero2).toFixed(2);
break;
case '*':
var resultado = (numero1 *
numero2).toFixed(2);
break;
case '/':
var resultado = (numero1 /
numero2).toFixed(2);
break;
}
// Mostrar el resultado en la caja de texto
document.getElementById("resultado").value =
resultado;
}
</script>
```

#### - Comentar el código y asegurarse de que esté bien indentado para una mayor claridad y presentación.

Se puede ver el código completo en [este documento](https://github.com/kelpygomez/dew/blob/main/Tarea-1/index.html).
