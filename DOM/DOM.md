> # Modulo 1 - Clase 03: DOM (Document Object Model)
---

> ## Render:
Proceso en el cual se cargan los elementos de una pagina web.

> ## DOM:
El DOM es una representación estructurada de una página web. Se parece a un árbol, donde cada etiqueta HTML es un nodo, incluyendo textos e imágenes.

> ## CSSOM:
El CSSOM es un modelo que representa los estilos asociados al DOM. El CSSOM es similar al DOM, pero se enfoca en el estilo de la página.

> ## RENDER TREE:
El Render Tree, es una combinación del DOM y el CSSOM que se enfoca únicamente en aquellos elementos del documento HTML que son visibles en la página. Este árbol representa todos los elementos visuales de la página y sus estilos, y es lo que el navegador utiliza para pintar la página en la pantalla.

> ## Layout:
El layout de una página determina el tamaño del dispositivo de salida (viewport) dando así contexto a los estilos que dependen de él. Este viewport puede ser configurado dentro de la etiqueta meta donde podemos modificar sus medidas y la escala inicial de mi página. El layout es el cálculo de las posiciones y tamaños de los elementos en la página. Antes de pintar los elementos, el navegador necesita saber dónde y qué tan grandes deben ser.

> ## Document Object Model:
El Document Object Model (DOM), es una estructura jerárquica en forma de árbol que representa todos los elementos de una página web. Para crear este objeto DOM, el navegador que lee el documento HTML toma parte por parte de este archivo, desde el elemento html (también llamado root) hasta las últimas etiquetas, y devuelve un objeto basado en su estructura y cuyo comportamiento será controlado a través de scripts JS.

> ## DOM API (Document Object Model Application Programming Interface):
Es un conjunto de interfaces y métodos proporcionados por los navegadores para permitir que los scripts de nuestro código interactúen con el DOM.
Es gracias a esta serie de métodos que podemos manipular, transformar y crear elementos dentro de un página web.

> ## Acciones que permiten realizar el DOM API:
1. Selección de elementos: Permitir la identificación y selección de elementos en el DOM, ya sea por etiqueta, clase, ID u otros selectores CSS.

2. Manipulación de contenido: Crear, modificar o eliminar el contenido de los elementos, como atributos, textos, etc.

3. Estilo y presentación: Modificar el estilo de los elementos para cambiar aspectos como el color, tamaño, posición, etc.

4. Eventos: Asociar funciones o scripts a eventos del usuario, como clics, teclas presionadas, entre otros, para crear interactividad.

5. Navegación: Recorrer la estructura del DOM, accediendo a nodos padres, hijos o hermanos.

> ## Selectores:
Son aquellos métodos y propiedades que nos permiten seleccionar elementos específicos de una página web, sin necesidad de afectar la naturaleza y el comportamiento de otros elementos del DOM.

> ## Eventos:
Son interacciones/acciones que podemos tener con los elementos que seleccionamos por media de selectores.

> ## Event listener:
Métodos que se complementan con los eventos. Estas funciones son las disparadoras de una lógica al momento de realizarse un evento.

Claro, aquí está el código que me enviaste:

```javascript
// Selecciona el botón por su ID
const loginButton = document.getElementById('loginButton');

// Función que se ejecutará cuando se haga click en el botón
function handleLoginClick() {
    console.log('Iniciando sesion ...');
}

// Agrega el evento de click al botón
loginButton.addEventListener('click', handleLoginClick);
```

> ## Metodos:
|Metodo|Funcion|
|:----:|:-----:|
|document.getElementById(id)|Retorna una referencia al elemento del DOM que tiene el id especificado.
|document.getElementsByClassName(className)|Retorna una colección de elementos del DOM que tienen la clase CSS especificada.
|document.querySelector(selector)|Retorna el primer elemento del DOM que coincide con el selector CSS especificado.
|document.querySelectorAll(selector)|Retorna todos los elementos del DOM que coinciden con el selector CSS especificado.
|element.textContent|Permite acceder o modificar el contenido de texto de un elemento.
|element.appendChild(childElement)|Agrega un nuevo hijo al final de la lista de hijos de un elemento.
|element.classList.add(class)|Permite agregarle clases al elemento.
|element.id|Permite asignarle un identificador unico al elemento.
|element.innerHTML|Permite agregar, modificar y eliminar los nodos hijos del elemento seleccionado.
|element.innerText|Permite definir el texto que contendra el elemento seleccionado.