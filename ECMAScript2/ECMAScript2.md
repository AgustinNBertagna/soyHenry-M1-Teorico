> # Modulo 1 - Clase 02: ECMAScript 2
---

> ## Arrow Function:
Manera de escribir funciones, pero con una sintaxis simplificada. Maneja diferente el objeto this.

```javascript
const suma = (a, b) => {
    return a + b
}
```

```javascript
const arr = ["🍔", "🥗", "🍇"];

// función tradicional
arr.forEach(function (elemento) {
  console.log(elemento);
});

// función flecha
arr.forEach((elemento) => console.log(elemento)); // 🍔 🥗 🍇

```
Cuando trabajamos con funciones tradicionales, la palabra reservada this se encuentra determinada por el contexto de la función que la contiene. Sin embargo, este comportamiento no es igual en las arrow functions, ya que, en este caso, la referencia de this se hereda del contexto léxico. Es decir, la referencia se toma del ámbito que contiene a la arrow function en el momento de su definición y no dentro de la función como tal.

> ## This: 
Si necesitas mantener el valor de this del ámbito circundante, las funciones flecha heredan el valor de this del contexto léxico en el que fueron creadas. Esto es útil en callbacks, funciones anidadas y cuando buscas evitar problemas relacionados con el cambio de contexto.

> ## Callbacks: 
En funciones callbacks donde la concisión y la captura del contexto son beneficiosas, las funciones flecha son útiles al trabajar con métodos como map, filter y reduce. Reducen la necesidad de funciones anónimas adicionales y brindan un código más limpio.

> ## Herencia: 
Cuando se desea evitar problemas relacionados con el binding de this, las funciones tradicionales pueden tener problemas cuando se utilizan en situaciones donde el valor de this cambia (por ejemplo, en eventos de DOM). Las funciones flecha eliminan este problema al heredar this del ámbito circundante.

> ## Clases:
Las "clases" son esencialmente plantillas para crear estos objetos, definiendo sus atributos y comportamientos.
Los objetos que provienen de dicha plantilla se conocen como instancias de clase (objetos).
Cada clase es una abstracción que define un conjunto de atributos y métodos que la componen.

> ## Encapsulamiento:
El  encapsulamiento  en es el principio de ocultar los detalles internos de la implementación de un objeto, exponiendo solo las interfaces necesarias para interactuar con él. Esto asegura la integridad de los datos y la seguridad de la implementación.

```javascript
class CajaFuerte {
    constructor() {
        this._dinero = 0; // Detalle interno oculto
    }

    depositar(cantidad) { this._dinero += cantidad }

    retirar(cantidad) {
        if (cantidad <= this._dinero) {
            this._dinero -= cantidad;
            return cantidad;
        }
        return 0;
    }
}
```

> ## Herencia:
La herencia es un principio que le permite a una clase derivar propiedades y métodos de otra clase, promoviendo la reutilización de código y la jerarquía en la estructuración de clases.

```javascript
class Padre {
    caminar() {
        console.log("Caminando.... ");
    }
}

class Hijo extends Padre {
    // Hijo hereda la capacidad de caminar de Padre
}

let hijo = new Hijo();
hijo.caminar(); // Muestra "Caminando.... "
```

> ## Polimorfismo:
El polimorfismo es una capacidad que permite que objetos de diferentes clases respondan a métodos con el mismo nombre, cada uno según su propia implementación.

```javascript
class Forma {
    dibujar() {
        console.log("Dibujando una forma genérica");
    }
}

class Circulo extends Forma {
    dibujar() {
        console.log("Dibujando un círculo");
    }
}

class Cuadrado extends Forma {
    dibujar() {
        console.log("Dibujando un cuadrado");
    }
}
```
> ## Abstracción:
La abstracción es el proceso de ocultar los detalles complejos de la implementación y exponer solo las características esenciales y las funcionalidades de un objeto.

```javascript
class Coche {
    constructor() {
        this._motorEncendido = false; // Propiedad privada
    }

    _encenderMotor() {
        // Método privado: Detalle interno sobre cómo se enciende el motor
        this._motorEncendido = true;
        console.log("Motor encendido");
    }

    _apagarMotor() {
        // Método privado: Detalle interno sobre cómo se apaga el motor
        this._motorEncendido = false;
        console.log("Motor apagado");
    }
}
```

> ## Constructor:
El constructor es un método especial dentro de una clase que se ejecuta automáticamente al crear un objeto de esa clase. Este método establece las propiedades iniciales del objeto basándose en los argumentos que recibe.

> ## Propiedades:
Las propiedades son variables que se encuentran dentro de una clase y que contienen información acerca del estado de un objeto.
Es importante tener en cuenta que aquellos valores que le queramos dar ala instancia de una clase deben ser recibidos como parámetros mediante el constructor.

> ## Metodos:
Los métodos son funciones definidas dentro de una clase que describen las acciones o comportamientos de los objetos creados a partir de esa clase.

> ## Instancia:
Una instancia es un objeto específico creado a partir de una clase. Cuando se utiliza el constructor de una clase para crear un nuevo objeto, ese objeto es una instancia de esa clase.
Es importante tener en cuenta que, para crear una instancia, en necesario utilizar la palabra reservada new y pasar los argumentos necesarios a la clase. Caso contrario, estos tendrán el valor undefined.

```javascript
class SuperHeroe {
    constructor(nombre, identidad, superpoder) { //constructor
        this.nombre = nombre; //propiedad
        this.superpoder = superpoder;
        this.identidad = identidad;
    }

    volar() { //metodo
        console.log("Mi nombre es", this.nombre)
    }
}

let superman = new SuperHeroe("Superman", "Clark Ken", ["Volar", "Fuerza"]) //instancia
superman.volar();  // 'Estoy volando'
```

> ## Super:
Constructor de la clase padre de una clase hija, a esta se le deben pasar por parametros las propiedades de la clase padre que la clase hija quiere heredar.