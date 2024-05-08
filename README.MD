<h1>ANALISIS DE CODIGO FUENTE</h1>

<h1>Primero</h1>

(() => {
    const devolverPrimerElemento = (array) => {
    if(array.length === 0) return {"message": "El arreglo no puede estar vacio"}
    if(!Array.isArray(array)) return {"message": "El parámetro debe ser un arreglo"}
    return array[0];
}
    console.log(devolverPrimerElemento([1,2,3,4,5]));
    console.log(devolverPrimerElemento([1]));
    console.log(devolverPrimerElemento([]));
    console.log(devolverPrimerElemento("Hola mundo"));
    console.log(devolverPrimerElemento(5));
    console.log(devolverPrimerElemento({}));
})();

<h1>Explicacion</h1>
Es una funcion de flecha en donde se verifica : Que el array no este vacio y que el parametro sea un array.Luego si el parametro enviado es un array y no esta vacio,retornara el primer elemento.

<h1>Segundo</h1>

 function devolverUltimoElemento(array) {
     if(array.length === 0) {
         return "No hay elementos en el array";
 }
 if(!Array.isArray(array)) {
     return "El parámetro no es un array";
 }
 return array.at(-1);
}
console.log(devolverUltimoElemento([1,2,3,4,5]));
console.log(devolverUltimoElemento(["Hola", "mundo"]));
console.log(devolverUltimoElemento([1]));
console.log(devolverUltimoElemento([]));
console.log(devolverUltimoElemento("Hola mundo"));
console.log(devolverUltimoElemento(5));
console.log(devolverUltimoElemento({}));

<h1>Explicacion</h1>
Es igual a el primer ejercicio solo que esta si todo esta bien retornara el ultimo valor.

<h1>Tercero</h1>

 function obtenerLargoDelArray(array) {
      return (!Array.isArray(array) ? "El parámetro no es un arreglo." : array.length);
}

console.log(obtenerLargoDelArray([1,2,3,4,5,6,7,8,9,10]));
console.log(obtenerLargoDelArray([]));
console.log(obtenerLargoDelArray({}));
console.log(obtenerLargoDelArray(1));
console.log(obtenerLargoDelArray("Hola"));

<h1>Explicacion</h1>
Se esta usando el operador ternario el es para evaluar si es un array,si es un array retornara el tamaño del mismo con "array.length"

<h1>Cuarto</h1>

 function arrayContiene(array, elemento) {
     if(!Array.isArray(array)){
        return "El primer argumento debe ser un arreglo"
 }
 return array.includes(elemento);
}
console.log(arrayContiene([1, 2, 3], 1)); // true
console.log(arrayContiene([1, 2, 3], 4)); // false\*/
console.log(arrayContiene(3, 4));
console.log(arrayContiene(["Pedro", "Juan", "Maria"], "Juan")); // true

<h1>Explicacion</h1>
Esta funcion recibe dos parametros que son array y un elemento el cual se buscara dentro del mismo.Si el array contiene tal elemento retornara "true" y en caso contrario retornara "false"

<h1>Quinto</h1>

 function numeroMasGrande(arrayOfNums) {
     if(!Array.isArray(arrayOfNums)) return "El parametro debe ser un arreglo"
     if(arrayOfNums.some((item) => typeof item !== "number")) return "Los elementos deben ser numeros"
     return arrayOfNums.reduce((acc, curr) => acc + curr, 0)
}
console.log(numeroMasGrande([1,2,3,4,5]));
console.log(numeroMasGrande([]));
console.log(numeroMasGrande([1,2,3,4,"5"]))
console.log(numeroMasGrande(6))
console.log(numeroMasGrande({}))
console.log(numeroMasGrande(false))

<h1>Explicacion</h1>
Esta funcion recibe "arrayOfNums" es decir, un array de numeros como unico parametro,verifica si el parametro es un array y si esta compuesto por numeros,luego buscara el amyor de los numeros y lo retornara

<h1>Sexto</h1>

 function empiezaConNueve(num) {
     if(typeof num !== "number") return "El parametro debe ser un numero";
     const numeroAString = String(num)
     const primerDigito = Number(numeroAString[0]);
     return primerDigito === 9
}
console.log(empiezaConNueve(965))
console.log(empiezaConNueve(65))
console.log(empiezaConNueve(999))
console.log(empiezaConNueve(0))
console.log(empiezaConNueve(9))
console.log(empiezaConNueve(true))

<h1>Explicacion</h1>
Se le da un parametro que es un numero,verifica que lo sea y pasa a convertirlo de numero a string con "string(num)"para luego verificar si el primero es un numero(9) si lo es retornara"true" en caso contrario "false"
