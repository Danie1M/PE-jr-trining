### 1 Creación de objetos: Crea un objeto para representar un libro, que incluya propiedades para el título, el autor y el año de publicación.

```js
let libro = {
  titulo: "Origen",
  autor: "Dan Brown",
  año: 2019,
};
```

### 2 Acceso a las propiedades de un objeto: Accede a cada una de las propiedades del objeto que creaste en el ejercicio 1 e imprímelas.

```js
console.log("titulo: ", libro.titulo);
console.log("autor: ", libro.autor);
console.log("año: ", libro.año);
```

### 3 Modificar propiedades de un objeto: Cambia el valor de la propiedad "año de publicación" en el objeto del ejercicio 1.

```js
libro.año = 2020;
console.log("3.- ", libro);
```

### 4 Agregar propiedades a un objeto: Agrega una nueva propiedad al objeto del ejercicio 1, como la cantidad de páginas del libro.

```js
libro["páginas"] = 640;
console.log("4.- ", libro);
```

### 5 Eliminar propiedades de un objeto: Utiliza el operador delete para eliminar la propiedad que agregaste en el ejercicio 4.

```js
delete libro.páginas;
console.log("5.- ", libro);
```

### 6 Recorrer las propiedades de un objeto: Utiliza un bucle for...in para recorrer todas las propiedades del objeto del ejercicio 1 e imprimir su nombre y valor.

```js
for (let ind in libro) {
  console.log(ind, ": ", libro[ind]);
}
```

### 7 Uso de métodos en objetos: Añade un método al objeto del ejercicio 1 que retorne una cadena con una descripción completa del libro.

```js
libro.descripcion = function () {
  const descr =
    "El libro , genera consiencias sobre como los cambios que se viven día a dia";
  console.log(descr);
};

console.log(libro);
```

### 8 El operador this en métodos de objetos: Modifica el método del ejercicio 7 para que utilice this para acceder a las propiedades del objeto.

```js
let libro2 = {
  titulo: "Origen",
  autor: "Dan Brown",
  año: 2019,
  descripcion: function () {
    const descr =
      "El libro " +
      this.titulo +
      ", genera consiencias sobre como los cambios que se viven día a dia";
    console.log(descr);
  },
};
console.log(libro2.descripcion());
```

### 9 Optional chaining: Crea un objeto con propiedades anidadas y utiliza el operador optional chaining (?.) para acceder a una propiedad que puede no existir.

```js
let carro = {
  color: "Rojo",
  marca: "Ford",
  modelo: 2015,
  pickup: false,
  accesorios: {
    bolsaAire: true,
    rines: "deportivos",
    sistemaFrenado: "ABS",
  },
};
console.log(carro.accesorios?.bolsaAire); /// true
console.log(carro.detalles?.dimension); /// undefined
```

### 10 Nullish coalescing operator: Crea un objeto con una propiedad que puede ser null o undefined y utiliza el operador Nullish coalescing (??) para proporcionar un valor por defecto.

```js
carro.accesorios.bolsaAire = null;
console.log((carro.accesorios.bolsaAire ??= "No agregado"));
```
