### 1 Definición de funciones: Define una función utilizando tanto una declaración de función como una expresión de función.

```js
function concatena(a, b) {
  return a + " " + b;
}

let suma = function (a, b) {
  return a + b;
};
console.log("Mi nombre es: ", concatena("Omar", "Daniel"));
console.log("suma : ", suma(12, 30));
```

### 2 Parámetros y argumentos: Define una función que tome dos parámetros y los sume. Llama a la función con dos argumentos y registra el resultado.

```js
let suma = function (a, b) {
  return a + b;
};
console.log("2.- suma : ", suma(8, 8));
```

### 3 Funciones anónimas: Crea una función anónima que retorne la longitud de una cadena dada. Asigna esta función a una variable y luego usa esta variable para llamar a la función.

```js
let longitud = function (cadena) {
  return cadena.length;
};
console.log("3.- ", longitud("Usuario"));
```

### 4 Funciones de flecha: Convierte la función anónima del ejercicio 3 en una función de flecha.

```js
let longitud2 = (cadena) => {
  return cadena.length;
};
console.log("4.- ", longitud2("contraseña"));
```

### 5 Funciones como valores: Crea una función que acepte otra función como parámetro. Llama a esta función con una función de flecha como argumento.

```js
let nombreLong = (concatena) => {
  return longitud(concatena);
};
console.log("5.-", nombreLong(concatena("Juan", "Perez Her")));
```

### 6 El objeto this en funciones globales: Crea una función en el ámbito global que imprima el valor de this. ¿Qué valor obtienes?

```js
function imprimeThis() {
  console.log("this: ", this); /// imprime el objeto Window {window: Window, self: Window, document: document, name: '', location: Location, …}
}
imprimeThis();
```

### 7 El objeto this en métodos de objetos: Crea un objeto con un método que imprima el valor de this. ¿Qué valor obtienes cuando llamas a este método?

```js
let mascota = {
  nombre: "Felix",
  meses: 3,
  enunciado: function () {
    const enun =
      "Mi mascota " + this.nombre + " tiene " + this.meses + " meses";
    console.log(enun);
  },
};
console.log(mascota.enunciado());
```

### 8 Uso de funciones dentro de otras funciones: Crea una función que defina una segunda función interna. Esta segunda función deberá acceder a una variable de la función externa. Luego, llama a la función externa y observa el resultado.

```js
let multi = (a, b) => {
  let multi = a * b;
  let rango = (multi) => {
    if (multi > 100) return true;
    else return false;
  };
  console.log(rango(multi));
  return multi;
};
console.log(multi(14, 6));
```

### 9 El objeto this en funciones de flecha: Crea una función de flecha en el ámbito global y otra como método de un objeto. En cada caso, imprime el valor de this. ¿Qué valor obtienes?

```js
function producto(nombre, precio) {
  this.nombre = nombre;
  this.precio = precio;
  let mensaje;
  if (precio <= 0) mensaje = "Error en captura de " + nombre;
  return mensaje;
}

console.log(mascota.enunciado());
console.log(producto("galletas", 0));
```

### 10 El objeto this y el método call: Crea un objeto con un método que use this. Usa el método call para cambiar el contexto de this cuando llames a este método.

```js
let persona = {
  nombre: "Daniel",
  genero: "Masculino",
  descricion: function () {
    console.log("La persona ", this.nombre, " vive en la zona centro.");
  },
};
let secundario = {
  nombre: "Omar",
};
persona.descricion.call(secundario);
```
