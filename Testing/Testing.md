> # Modulo 1 - Clase 04: Testing
---

> ## Testing:
El testing es un área que se enfoca en evaluar el comportamiento del código de forma controlada. Los tests son ejecutados de forma aislada.

> ## TDD (Testing Driven Development):
Esta metodología nos dice que primero debemos desarrollar un test que facilite la solución de un problema. Y luego, hay que comenzar a desarrollar el código a partir de los tests.

> ## Tipos de Testing:
1. UNIT:
    * Son los más sencillos y simples de implementar.
    * Evalúan porciones o pequeñas parte de código de forma individual.
    * Trabajan con funciones puras, es decir, que para un mismo input siempre van a devolver el mismo output.

2. INTEGRATION:
    * Se enfocan en la integración del código.
    * Evalúa cómo funcionan de forma conjunta varios bloques o implementaciones del código de nuestra app y la interacción entre estas. Por ejemplo, la comunicación de un servidor con la base de datos.

3. AUTOMATION:
    * UI tests: Se enfocan en evaluar todo el comportamiento de las interacciones del cliente con nuestra interfaz.
    * End-to-end: Se enfocan en el flujo completo de nuestra aplicación.

> ## Tests Unitarios:
Pequeñas funciones que verifican el comportamiento de unidades específicas del software de manera automatizada. Su objetivo principal es asegurar que cada unidad funcione correctamente de manera individual y en conjunto con otras unidades. 

1. UNIDAD DE PRUEBA: Un test unitario se centra en evaluar una "unidad" específica de código. Esta unidad puede ser una función, método o clase, y la idea es aislarla del resto del sistema para validar su comportamiento de manera independiente.

2. ESCRIBIR EL TEST: El desarrollador escribe un test que verifica un aspecto específico de una pieza de código. Establece condiciones iniciales, llama a la unidad que se está probando y evalúa el resultado en función de las expectativas.

3. EJECUCIÓN DEL TEST: Los tests unitarios se ejecutan de manera automática. Este proceso puede ser parte de un flujo de construcción más amplio o ejecutarse por separado, dependiendo de la configuración del proyecto.

4. RESULTADO DEL TEST: Si la unidad de código funciona correctamente, el test pasa satisfactoriamente. Si hay algún error o el comportamiento no cumple con las expectativas, el test fallará y deberá reescribirse para luego volver a probar. La salida del test proporciona información sobre qué parte específica del código no está funcionando como se esperaba.

5. REFACTORIZACIÓN: Luego del test, los desarrolladores pueden refactorizar el código para mejorarlo sin cambiar su comportamiento externo. La existencia de tests unitarios sólidos facilita la refactorización, ya que cualquier cambio no deseado se destacará a través de los tests.

> ## BDD (Behavior Driven Development):
Metodologia de desarrollo dirigido por comportamiento que se basa en definir los casos de prueba en un idioma común entre todos los stakeholders. A diferencia de TDD (Test Driven Development), BDD se enfoca en la prueba de más alto nivel, la funcionalidad de aceptación, y facilita la testeabilidad del sistema.

> ## Framework:
Los frameworks son tecnologías ya desarrolladas que permiten desarrollar aplicaciones de manera más sencilla y eficiente.
* Metodos: Ya diseñados para que le demos un uso adecuado a la herramienta.

* Estructura: Una arquitectura predefinida para que nuestra aplicación sea prolija y escalable.

* Buenas Prácticas: Permite que otros devs que usen esta herramienta puedan comprender lo que hemos escrito.

> ## Jasmine:
Framework orientado al desarrollo de testing para aplicaciones.

> ## Características de Jasmine:

* Claridad en sintaxis: A diferencia de otras tecnologías de testing, Jasmine utiliza una sintaxis clara y descriptiva, incluso para aquellos que no están directamente involucrados en el desarrollo.

* Suite y especificación: Permite organizar los tests con un orden de jerarquía ("suites" y "especificaciones"), proporcionando una estructura lógica para su ejecución.

* Mocks: Facilita la creación de contenido falso o de prueba (mockeo) para simular el comportamiento de la aplicación como si fuera tiempo real.

> ## Expect & Matchers:
EXPECTS:
Es una función central en Jasmine que se utiliza para comenzar una declaración de testing.
Se utiliza para retornar un objeto especial que representa el valor que se está evaluando y proporciona métodos (llamados matchers) para realizar afirmaciones sobre ese valor.

MATCHERS:
Son métodos adjuntos al objeto devuelto por expect que permiten hacer comparaciones y afirmaciones en las pruebas.

```javascript
describe("Nombre Del Test General", function () {
    it("Nombre del test unitario", function () {
        expect(5 + 5).toBe(10) //expect es el expect propiamente hablando, toBe en este caso es el matcher.
    })
})
```