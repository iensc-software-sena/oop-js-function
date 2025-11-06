# IENSCH

---

# Clase: Funciones en JavaScript

---

## 🎯 Objetivo de la clase

Comprender el concepto de **función** en **JavaScript**, su estructura, utilidad y 
cómo nos ayuda a **organizar**, **reutilizar** y **mantener** más limpio el código.  
Aprenderemos diferentes tipos de funciones y aplicaremos su uso mediante ejercicios 
prácticos.

---

## 🧠 ¿Qué es una función?

Una **función** es un bloque de código que realiza una tarea específica y puede 
reutilizarse en diferentes partes del programa.  
En otras palabras, una función **recibe datos, los procesa y devuelve un resultado**.

Las funciones son muy útiles porque:

- Evitan repetir código.
- Mejoran la organización del programa.
- Hacen el código más fácil de leer, mantener y probar.

---

## 🧩 Sintaxis básica

```js
function nombreDeLaFuncion(parámetros) {
  // bloque de código
  return valor; // (opcional)
}
```

#### Elementos principales:

- `function`: palabra reservada que indica que se va a declarar una función.
- `nombreDeLaFuncion`: nombre que identifica la función.
- parámetros: valores de entrada que recibe la función (opcional).
- return: valor que devuelve la función (opcional).

## 📘 Tipos de funciones en JavaScript

#### 1. Función declarada

Estas funciones se definen con la palabra clave **`function`** y pueden ser llamadas 
antes o después de su declaración gracias al **hoisting**.

```js
function saludar() {
  console.log("¡Hola a todos!");
}

saludar(); // ¡Hola a todos! 
```

#### 2. Función con parámetros

Podemos enviar datos a la función para que los utilice dentro de su bloque.

```js
function saludarPersona(nombre) {
  console.log("Hola " + nombre + "!");
}

saludarPersona("Tony Stark"); // Hola Tony Stark!
```

#### 3. Función con retorno de valor

Cuando una función usa **`return`**, devuelve un resultado que puede almacenarse 
o utilizarse en otro lugar del código.

```js
function sumar(a, b) {
  return a + b;
}

const resultado = sumar(5, 3);
console.log("La suma es: ", resultado); // La suma es: 8
```

#### 4. Función anónima

Una función anónima no tiene nombre y suele asignarse a una variable o usarse 
como argumento en otra función.

```js
const restar = function(a, b) {
  return a - b;
};

console.log(restar(10, 4)); // 6
```

### 5. Función flecha (Arrow Function)

Las arrow functions son una forma más moderna y compacta de escribir funciones.
No tienen su propio contexto de `this` y son muy usadas en programación funcional 
y orientada a objetos.

```js
const multiplicar = (a, b) => a * b;

console.log(multiplicar(4, 2)); // 8
```

También pueden usarse sin parámetros o con un solo parámetro:

```js
const saludar = () => console.log("Hola mundo!");
const cuadrado = n => n * n;

saludar(); // Hola mundo!
console.log(cuadrado(5)); // 25
```

---

## 💡 Buenas prácticas al usar funciones

- Usa nombres descriptivos que indiquen lo que hace la función.
    Ejemplo: **`calcularPromedio()`**, **`obtenerEdad()`**, **`convertirTemperatura()`**.
- Crea funciones cortas y específicas (una función = una responsabilidad).
- Evita usar variables globales dentro de funciones si no es necesario.
- Comenta las funciones que tengan lógica compleja.
- Reutiliza funciones en lugar de repetir código.

---

## ⚙️ Ejemplos prácticos

### Ejemplo 1: Sumar números

```js
function sumar(a, b) {
  return a + b;
}

console.log(sumar(10, 20)); // 30
```

### Ejemplo 2: Calcular el área de un triángulo

```js
function calcularAreaTriangulo(base, altura) {
  return (base * altura) / 2;
}

console.log(calcularAreaTriangulo(5, 8)); // 20
```

### Ejemplo 3: Determinar si una persona es mayor de edad

```js
function esMayorDeEdad(edad) {
  if (edad >= 18) {
    return true;
  } else {
    return false;
  }
}

console.log(esMayorDeEdad(21)); // true
```

---

## 🧮 Ejercicios para desarrollar en clase

### 🧩 Ejercicio 1:

Crear una función llamada **`esPar(numero)`** que reciba un número y retorne **true** 
si es par o **false** si es impar.

Ejemplo:

```js
esPar(4); // true
esPar(7); // false
```

### 🧩 Ejercicio 2:

Crear una función llamada **`calcularPromedio(n1, n2, n3)`** que reciba tres notas 
y retorne el promedio. Luego imprimir un mensaje que diga si el estudiante aprueba 
(>=3.0) o reprueba (<3.0).

Ejemplo:

```js
calcularPromedio(4.0, 3.5, 5.0); // 4.16 -> "Aprobado"
```

### 🧩 Ejercicio 3:

Crear una función llamada **`convertirTemperatura(Celsius)`** que convierta grados 
**Celsius** a **Fahrenheit**.

La fórmula es:

> F = (C × 9/5) + 32

Ejemplo:

```js
convertirTemperatura(0); // 32
convertirTemperatura(25); // 77
```

### 🧠 Ejercicio adicional (reto):

Crear una función llamada **`calcularDescuento(precio, porcentaje)`** que reciba 
el precio original de un producto y un porcentaje de descuento, y retorne el nuevo
 precio con el descuento aplicado.

Ejemplo:

```js
calcularDescuento(100, 20); // 80
```

---

## 📚 Conclusión

Las funciones son una base fundamental en la programación.
Permiten crear **código modular, reutilizable y fácil de mantener**.
En la **Programación Orientada a Objetos**, las funciones se convertirán más adelante 
en **métodos** dentro de las **clases**, desempeñando un papel clave en la lógica de los
**objetos**.

## 💬

> “Piensa en las funciones como pequeñas máquinas: 
> reciben algo, lo transforman, y devuelven un resultado.”