### 1 Creación de arreglos: Crea un arreglo con cinco elementos y registra su longitud.

```js
let array = ["Carro", "Tren", "Trailer", "Moto", "Camion"];
console.log(array.length);
```

### 2 Acceso a los elementos del arreglo: Accede al primer y al último elemento del arreglo que creaste en el ejercicio 1.

```js
console.log(array[0], " ", array[4]);
```

### 3 Modificar elementos de un arreglo: Cambia el valor del tercer elemento en el arreglo que creaste en el ejercicio 1.

```js
array[2] = "Tracto Camion";
console.log("3: ", array);
```

### 4 Agregar elementos a un arreglo: Utiliza el método push para agregar un elemento al final del arreglo del ejercicio 1.

```js
array.push("Avión");
console.log("4: ", array);
```

### 5 Remover elementos de un arreglo: Utiliza el método pop para eliminar el último elemento del arreglo del ejercicio 1.

```js
array.pop();
console.log("5: ", array);
```

### 6 Recorrer un arreglo con un bucle for: Escribe un bucle for que recorra todos los elementos del arreglo del ejercicio 1 y los imprima.

```js
console.log("6.-");
for (let arra of array) {
  console.log(arra);
}
```

### 7 Recorrer un arreglo con el método forEach: Ahora utiliza el método forEach para hacer lo mismo que en el ejercicio 6.

```js
console.log("7.-");
array.forEach((element) => console.log(element));
```

### 8 Filtrar elementos de un arreglo: Crea un arreglo de números y utiliza el método filter para obtener un nuevo arreglo con solo los números que son mayores que 10.

```js
let numb = [20, 5, 15, 9, 30, 7, 4, 18, 11, 10];
let numFilter = numb.filter((elem) => elem > 10);
console.log(numFilter);
```

### 9 Transformar elementos de un arreglo: A partir del arreglo de números del ejercicio 8, utiliza el método map para obtener un nuevo arreglo donde cada número se haya multiplicado por 10.

```js
let numbMap = numb.map(function (x) {
  return x * 10;
});
console.log(numbMap);
```

### 10 Transformar elementos de un arreglo: A partir del arreglo de números del ejercicio 8, utiliza el método map para obtener un nuevo arreglo donde cada número se haya multiplicado por 10.

```js
let numbReduce = numb.reduce(function (x, y, indice, vector) {
  return x + y;
});
console.log(numbReduce);
```
