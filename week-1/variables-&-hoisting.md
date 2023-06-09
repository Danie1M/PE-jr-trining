### 1. Declaración de variables: Declara tres variables usando var, let y const. Asigna a cada una un valor de un tipo de dato diferente.

```js
var x = "Hola";
let y = true;
const z = 15;
```

### 2. Reasignación de variables: Intenta reasignar las variables declaradas en el ejercicio 1. ¿Qué sucede con cada tipo de variable?

```js
x = "Mundo";
y = 16;
//z = false;  /// Uncaught TypeError: Assignment to constant variable.
```

### 3 Alcance de las variables: Crea una función e intenta acceder a una variable let definida dentro de la función desde fuera de la función. ¿Qué sucede?

```js
function alcance() {
  let varAlcan = "Hola Mundo";
}
//console.log(varAlcan)   /// Uncaught ReferenceError: varAlcan is not defined
```

### 4 Alcance de las variables (parte 2): Ahora declara una variable var dentro de la función. ¿Puedes acceder a ella desde fuera de la función?

```js
function alcance() {
  var varAlcan2 = "Hola Mundo";
}
//console.log(varAlcan2)    /// Uncaught ReferenceError: varAlcan2 is not defined
```

### 5 Hoisting: Declara una variable con var después de un bloque de código que intenta acceder a esa variable. ¿Qué valor se obtiene al acceder a la variable antes de su declaración?

```js
function nombrePer5(nombre) {
  console.log("El nombre de la persona es: " + nombre); // Se ejecuta
}
var nombre_1 = "Daniel";
nombrePer5(nombre_1);
```

### 6 Hoisting (parte 2): Repite el ejercicio 5, pero esta vez con una variable let. ¿Qué sucede?

```js
function nombrePer6(nombre) {
  console.log("El nombre de la persona es: " + nombre); // Se ejecuta
}
let nombre_2 = "Daniel Mtz";
nombrePer6(nombre_2);
```

### 7 Hoisting de funciones: Declara una función después de un bloque de código que intenta llamar a esa función. ¿Se puede ejecutar la función antes de su declaración?

```js
function nombrePer7() {
  let nombre = "Omar Daniel";
  console.log("El nombre de la persona es: " + nombre + apellido()); // Se ejecuta
}
nombrePer7();

function apellido() {
  let apellido = " Mtz";
  return apellido;
}
```

### 8 Tipos de datos: Declara variables y asigna a cada una un valor de un tipo de datos diferente. Luego, utiliza typeof para verificar el tipo de cada variable.

```js
var nombre = "Hola";
let activo = true;
const date = "2018/07/22";
console.log(typeof nombre); /// string
console.log(typeof activo); /// boolean
console.log(typeof date); /// string
```

### 9 Conversión de tipos: Declara una variable con un número como una cadena (por ejemplo, "123"). Luego, intenta convertirlo en un número usando el objeto Number.

```js
let num = "687425";
console.log(Number(num)); /// 687425
```

### 10 Objetos y arrays: Declara una variable como un objeto con algunas propiedades y un array con algunos elementos. Luego, intenta agregar, modificar y eliminar propiedades y elementos.

```js
let obje = {
  nombre: "Daniel",
  apellido: "Martínez",
};
let arr10 = ["Gato", "perro"];

obje["date"] = "94/04/04";
obje.apellido = "González";
obje["pais"] = "México";
delete obje.pais;

arr10.push("conejo");
arr10.pop();

console.log(obje);
console.log(arr10);
```
