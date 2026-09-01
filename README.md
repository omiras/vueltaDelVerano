# JavaScript — Vuelta del parón

Este conjunto de ejercicios está pensado para repasar JavaScript después de un tiempo sin tocarlo.

- No es un examen.
- No importa equivocarte.
- Lo importante es intentar resolverlo y entender por qué funciona.

---

## ex1 — ¿Qué tipo es?

Concepto: en JavaScript, cada valor tiene un tipo. Los más básicos son `String` (texto), `Number` (números) y `Boolean` (verdadero/falso).

Sin ejecutar el código, indica qué tipo de dato contiene cada variable.

```js
const nombre = "Laura";
const edad = 27;
const activo = true;
const precio = 19.95;
const ciudad = "Girona";
```

Resultado esperado:

- nombre → String
- edad → Number
- activo → Boolean
- precio → Number
- ciudad → String

---

## ex2 — Cambia los valores

Concepto: una variable guarda un valor y luego podemos usarlo para formar mensajes. Las cadenas se pueden concatenar con `+`.

Crea estas variables y muestra una frase como la siguiente:

```js
const nombre = "Laura";
const edad = 27;
const tieneCarnet = true;

console.log(nombre + " tiene " + edad + " años y tiene carnet: " + tieneCarnet);
```

Resultado esperado:

```txt
Laura tiene 27 años y tiene carnet: true
```

---

## ex3 — ¿Funciona con let?

Concepto: `let` sirve para declarar variables que sí pueden cambiar su valor después.

```js
let edad = 25;

edad = 26;

console.log(edad);
```

Resultado esperado:

```txt
26
```

Explicación: `let` permite reasignar el valor.

---

## ex4 — ¿Funciona con const?

Concepto: `const` sirve para declarar una variable que no va a cambiar. Si intentas reasignarle un valor, JavaScript da error.

```js
const edad = 25;

edad = 26;

console.log(edad);
```

Resultado esperado:

```txt
Error: Assignment to constant variable.
```

Explicación: `const` no permite cambiar el valor una vez declarado.

---

## ex5 — Decide si usar `let` o `const`

Concepto: elegir `let` o `const` depende de si el valor va a modificarse o no.

```js
const nombrePersona = "Laura";
let contador = 0;
const precio = 19.99;
let intentosRestantes = 3;
const nombreCiudad = "Girona";
```

Resultado esperado:

- Nombre de una persona que no va a cambiar → `const`
- Contador que aumenta → `let`
- Precio de un producto que no cambia → `const`
- Número de intentos restantes → `let`
- Nombre de una ciudad → `const`

---

## ex6 — ¿Puede entrar?

Concepto: los condicionales permiten decidir entre dos caminos según una condición.

```js
const edad = 17;

if (edad >= 18) {
  console.log("Puedes entrar");
} else {
  console.log("No puedes entrar");
}
```

Resultado esperado:

```txt
No puedes entrar
```

---

## ex7 — Temperatura

Concepto: con `if`, `else if` y `else` podemos evaluar varios casos distintos.

```js
const temperatura = 31;

if (temperatura < 15) {
  console.log("Hace frío");
} else if (temperatura >= 15 && temperatura <= 25) {
  console.log("Temperatura agradable");
} else {
  console.log("Hace calor");
}
```

Resultado esperado:

```txt
Hace calor
```

---

## ex8 — ¿Qué imprime?

Concepto: `>=` significa “mayor o igual”, y el flujo se evalúa en orden desde el primer `if` hasta el que coincida.

```js
const puntos = 80;

if (puntos >= 90) {
  console.log("Excelente");
} else if (puntos >= 50) {
  console.log("Aprobado");
} else {
  console.log("Suspenso");
}
```

Resultado esperado:

```txt
Aprobado
```

---

## ex9 — Verdadero o falso

Concepto: las comparaciones devuelven `true` o `false`. El operador `===` compara valor y tipo.

```js
console.log(10 > 5);
console.log(10 === 10);
console.log(10 === "10");
console.log(8 < 3);
console.log(5 >= 5);
```

Resultado esperado:

```txt
true
true
false
false
true
```

Explicación:

- `10 > 5` → 10 es mayor que 5 → `true`
- `10 === 10` → mismo valor y mismo tipo → `true`
- `10 === "10"` → número y texto no son iguales → `false`
- `8 < 3` → 8 no es menor que 3 → `false`
- `5 >= 5` → 5 es igual o mayor que 5 → `true`

---

## ex10 — Mayor de edad

Concepto: usamos comparadores para comprobar relaciones entre números.

```js
const edad = 21;

console.log(edad === 18);
console.log(edad >= 18);
console.log(edad < 18);
```

Resultado esperado:

```txt
false
true
false
```

Explicación:

- `edad === 18` → es exactamente 18 → `false`
- `edad >= 18` → es mayor o igual que 18 → `true`
- `edad < 18` → es menor que 18 → `false`

---

## ex11 — Cuenta normal hasta 5

Concepto: un bucle `for` repite instrucciones un número determinado de veces.

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Resultado esperado:

```txt
1
2
3
4
5
```

---

## ex12 — Suma del 1 al 10

Concepto: una variable acumuladora guarda el resultado de cada iteración. Eso se llama “acumular”.

```js
let suma = 0;

for (let i = 1; i <= 10; i++) {
  suma += i;
}

console.log(suma);
```

Resultado esperado:

```txt
55
```

---

## ex13 — Longitud de una cadena

Concepto: `length` devuelve cuántos caracteres tiene una cadena.

```js
const nombre = "Alejandro";

console.log(nombre.length);
```

Resultado esperado:

```txt
9
```

---

## ex14 — Primera letra

Concepto: en JavaScript, una cadena se puede acceder por posición, al igual que un array. La primera posición es el índice `0`.

```js
const palabra = "JavaScript";

console.log(palabra[0]);
```

Resultado esperado:

```txt
J
```

---

## ex15 — Última letra

Concepto: para acceder a la última posición, usamos la longitud menos 1. Así se obtiene el último carácter.

```js
const palabra = "Programacion";

console.log(palabra[palabra.length - 1]);
```

Resultado esperado:

```txt
n
```

---

## ex16 — Recortar un texto con slice()

Concepto: `slice(inicio, fin)` devuelve una parte del texto. El índice final no se incluye.

```js
const palabra = "JavaScript";

console.log(palabra.slice(0, 4));
```

Resultado esperado:

```txt
Java
```

---

## ex17 — Las primeras letras de un nombre

Concepto: `slice()` permite obtener un trozo del texto desde una posición concreta hasta otra.

```js
const nombre = "Alejandro";

console.log(nombre.slice(0, 4));
```

Resultado esperado:

```txt
Alej
```

Explicación: `slice(0, 4)` toma desde el índice 0 hasta el índice 4, sin incluirlo. En "Alejandro", los primeros 4 caracteres son `A`, `l`, `e`, `j` → `Alej`.

---

## ex18 — Obtener el nombre de usuario de un email

Concepto: `slice()` sirve para recortar cadenas y obtener solo la parte que nos interesa.

```js
const email = "alumno@gmail.com";

console.log(email.slice(0, 6));
```

Resultado esperado:

```txt
alumno
```

Explicación: el correo empieza con `alumno` y luego viene `@gmail.com`. Con `slice(0, 6)` cogemos solo los 6 primeros caracteres.

---

## ex19 — Saludar

Concepto: una función permite reutilizar código. Recibe parámetros y ejecuta una tarea.

```js
function saludar(nombre) {
  console.log("Hola, " + nombre);
}

saludar("Laura");
saludar("Carlos");
```

Resultado esperado:

```txt
Hola, Laura
Hola, Carlos
```

---

## ex20 — Duplicar

Concepto: una función puede devolver un valor con `return`, y ese valor puede usarse después.

```js
function duplicar(numero) {
  return numero * 2;
}

console.log(duplicar(5));
```

Resultado esperado:

```txt
10
```

---

## ex21 — ¿Qué diferencia hay entre `console.log()` y `return`?

Concepto: `console.log()` muestra algo por pantalla, pero no devuelve un valor útil para seguir usándolo. `return` sí devuelve un resultado que puede almacenarse o reutilizarse.

```js
function sumar(a, b) {
  console.log(a + b);
}

function sumarConReturn(a, b) {
  return a + b;
}

const resultado = sumarConReturn(5, 3);
console.log(resultado);
```

Resultado esperado:

```txt
8
```

Explicación:

- `console.log()` muestra el valor en la consola, pero no lo devuelve para usarlo después.
- `return` devuelve un valor que puedes guardar en una variable o reutilizar.

---

## ex22 — Mayor de dos

Concepto: una función puede decidir qué valor devolver según una condición.

```js
function mayor(a, b) {
  if (a > b) {
    return a;
  } else {
    return b;
  }
}

console.log(mayor(10, 25));
```

Resultado esperado:

```txt
25
```

---

## ex23 — Acceder a elementos de un array

Concepto: un array es una lista ordenada. Cada elemento tiene una posición llamada índice, y empieza en `0`.

```js
const frutas = ["manzana", "plátano", "naranja", "pera"];

console.log(frutas[0]);
console.log(frutas[2]);
console.log(frutas[frutas.length - 1]);
```

Resultado esperado:

```txt
manzana
naranja
pera
```

---

## ex24 — Cambiar un elemento del array

Concepto: los arrays son mutables; podemos cambiar un valor concreto usando su índice.

```js
const colores = ["rojo", "verde", "azul"];

colores[1] = "amarillo";
console.log(colores);
```

Resultado esperado:

```txt
[ 'rojo', 'amarillo', 'azul' ]
```

---

## ex25 — Añadir un elemento con push()

Concepto: `push()` añade un nuevo elemento al final de un array.

```js
const alumnos = ["Ana", "Luis", "Marta"];

alumnos.push("Carlos");
console.log(alumnos);
```

Resultado esperado:

```txt
[ 'Ana', 'Luis', 'Marta', 'Carlos' ]
```

---

## ex26 — Recorrer un array con for

Concepto: un bucle `for` nos sirve para recorrer cada elemento del array y trabajar con ellos.

```js
const ciudades = ["Girona", "Barcelona", "Tarragona", "Lleida"];

for (let i = 0; i < ciudades.length; i++) {
  console.log(ciudades[i]);
}
```

Resultado esperado:

```txt
Girona
Barcelona
Tarragona
Lleida
```

---

## ex27 — Buscar aprobados

Concepto: combinar arrays y condicionales permite filtrar información y mostrar solo los elementos que cumplen una condición.

```js
const notas = [4, 7, 8, 3, 10, 5];

for (let i = 0; i < notas.length; i++) {
  if (notas[i] >= 5) {
    console.log(notas[i]);
  }
}
```

Resultado esperado:

```txt
7
8
10
5
```

---

## ex28 — ¿Hay suspensos?

Concepto: también podemos detectar si existe algún elemento que no cumple una condición.

```js
const notas = [7, 8, 6, 9, 5];

for (let i = 0; i < notas.length; i++) {
  if (notas[i] < 5) {
    console.log("Hay suspensos");
    break;
  }
}
```

Resultado esperado:

```txt
(no se imprime nada)
```

Explicación: este array no tiene ninguna nota menor que 5, así que no se muestra el mensaje.

---

## ex29 — Conocer un objeto

Concepto: un objeto guarda información en propiedades, con un nombre y un valor. Se accede con `objeto.propiedad`.

```js
const alumno = {
  nombre: "Laura",
  edad: 27,
  nota: 8
};

console.log(alumno.nombre);
console.log(alumno.edad);
console.log(alumno.nota);
```

Resultado esperado:

```txt
Laura
27
8
```

---

## ex30 — Modificar una propiedad

Concepto: los objetos también se pueden modificar cambiando el valor de una propiedad.

```js
const alumno = {
  nombre: "Laura",
  edad: 27,
  nota: 8
};

alumno.nota = 9;
console.log(alumno);
```

Resultado esperado:

```txt
{ nombre: 'Laura', edad: 27, nota: 9 }
```

---

## ex31 — Condición sobre un objeto

Concepto: podemos combinar objetos con condiciones para decidir qué mensaje mostrar.

```js
const alumno = {
  nombre: "Carlos",
  edad: 20,
  nota: 4
};

if (alumno.nota >= 5) {
  console.log(alumno.nombre + " ha aprobado");
} else {
  console.log(alumno.nombre + " ha suspendido");
}
```

Resultado esperado:

```txt
Carlos ha suspendido
```

---

## ex32 — Mostrar todos los hoteles

Concepto: un array puede contener objetos, y cada objeto puede tener varias propiedades.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  }
];

for (let i = 0; i < reservas.length; i++) {
  console.log(reservas[i].hotel);
}
```

Resultado esperado:

```txt
Hotel Sol
Hotel Mar
Hotel Playa
```

---

## ex33 — Precio de la primera reserva

Concepto: para acceder a propiedades dentro de un objeto del array, usamos la sintaxis `array[i].propiedad`.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  }
];

const primeraReserva = reservas[0];
console.log(primeraReserva.noches * primeraReserva.precio);
```

Resultado esperado:

```txt
240
```

---

## ex34 — Función para calcular el precio de una reserva

Concepto: una función puede recibir un objeto como parámetro y devolver un cálculo basado en sus propiedades.

```js
function calcularPrecio(reserva) {
  return reserva.noches * reserva.precio;
}

const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  }
];

console.log(calcularPrecio(reservas[0]));
```

Resultado esperado:

```txt
240
```

---

## ex35 — Reto final A: mostrar todos los hoteles

Concepto: se repite el recorrido de un array de objetos para extraer una propiedad concreta de cada elemento.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  },
  {
    hotel: "Hotel Montaña",
    noches: 7,
    precio: 50
  }
];

for (let i = 0; i < reservas.length; i++) {
  console.log(reservas[i].hotel);
}
```

Resultado esperado:

```txt
Hotel Sol
Hotel Mar
Hotel Playa
Hotel Montaña
```

---

## ex36 — Reto final B: precio total de cada reserva

Concepto: una operación matemática útil es multiplicar noches por precio para obtener el total de la reserva.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  },
  {
    hotel: "Hotel Montaña",
    noches: 7,
    precio: 50
  }
];

for (let i = 0; i < reservas.length; i++) {
  const total = reservas[i].noches * reservas[i].precio;
  console.log(reservas[i].hotel + ": " + total + " €");
}
```

Resultado esperado:

```txt
Hotel Sol: 240 €
Hotel Mar: 325 €
Hotel Playa: 240 €
Hotel Montaña: 350 €
```

---

## ex37 — Reto final C: mostrar reservas de más de 300 €

Concepto: con condicionales dentro de un bucle se pueden filtrar elementos según una regla concreta.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  },
  {
    hotel: "Hotel Montaña",
    noches: 7,
    precio: 50
  }
];

for (let i = 0; i < reservas.length; i++) {
  const total = reservas[i].noches * reservas[i].precio;
  if (total > 300) {
    console.log(reservas[i].hotel + ": " + total + " €");
  }
}
```

Resultado esperado:

```txt
Hotel Mar: 325 €
Hotel Montaña: 350 €
```

---

## ex38 — Reto final D: crear la función `calcularPrecio`

Concepto: encapsular lógica en funciones ayuda a reutilizar cálculos y mantiene el código más limpio.

```js
function calcularPrecio(reserva) {
  return reserva.noches * reserva.precio;
}

const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  }
];

console.log(calcularPrecio(reservas[0]));
```

Resultado esperado:

```txt
240
```

---

## ex39 — Reto final E: función `esReservaLarga`

Concepto: una función booleana devuelve `true` o `false` según cumpla o no una condición.

```js
function esReservaLarga(reserva) {
  return reserva.noches >= 5;
}

const reserva = {
  hotel: "Hotel Mar",
  noches: 5,
  precio: 65
};

console.log(esReservaLarga(reserva));
```

Resultado esperado:

```txt
true
```

---

## ex40 — Reto final F: usar `slice()` sin modificar el array original

Concepto: `slice()` crea una copia de una parte del array o texto, sin tocar el original. Esto es muy útil cuando queremos conservar los datos iniciales.

```js
const reservas = [
  {
    hotel: "Hotel Sol",
    noches: 3,
    precio: 80
  },
  {
    hotel: "Hotel Mar",
    noches: 5,
    precio: 65
  },
  {
    hotel: "Hotel Playa",
    noches: 2,
    precio: 120
  },
  {
    hotel: "Hotel Montaña",
    noches: 7,
    precio: 50
  }
];

const primerasDos = reservas.slice(0, 2);
console.log(primerasDos);
console.log(reservas.length);
```

Resultado esperado:

```txt
[
  { hotel: 'Hotel Sol', noches: 3, precio: 80 },
  { hotel: 'Hotel Mar', noches: 5, precio: 65 }
]
4
```

Explicación: `slice(0, 2)` crea un nuevo array con los primeros dos elementos. El array original `reservas` sigue intacto.

---

## Preguntas para terminar

1. ¿Qué concepto recordabas mejor?
2. ¿Qué concepto habías olvidado?
3. ¿Qué te ha parecido más fácil?
4. ¿Qué te ha parecido más difícil?
5. ¿Qué diferencia hay entre un array y un objeto?
6. ¿Qué diferencia hay entre `console.log()` y `return`?
7. ¿Para qué sirve una función?
8. ¿Para qué sirve `slice()`?
9. ¿Qué significa que una función reciba un parámetro?
10. Si tuvieras que explicarle JavaScript a alguien que nunca lo ha visto, ¿por dónde empezarías?

---

## Resumen rápido

- `const` → valor fijo, no se reasigna.
- `let` → valor que puede cambiar.
- `if` / `else if` / `else` → decisiones.
- `for` → repeticiones.
- `function` → bloques reutilizables.
- `return` → devuelve un valor para usarlo.
- `console.log()` → muestra información en la consola.
- `slice()` → corta partes de texto o arrays sin modificar el original.
