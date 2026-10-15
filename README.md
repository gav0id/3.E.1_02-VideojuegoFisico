Ejercicio 3.E.1 02 - Cadena de Constructores (VideojuegoFisico)

Lógica del programa
Para este segundo ejercicio, el objetivo fue analizar el orden en el que la Máquina Virtual de Java (JVM) ejecuta los constructores cuando existe una jerarquía de herencia. 

Reutilicé la superclase `ProductoGeek` y creé la subclase `VideojuegoFisico` utilizando la palabra clave `extends`, añadiéndole los atributos específicos `plataforma` (String) y `pesoGramos` (double).

Para poder observar el proceso de construcción en memoria, agregué un mensaje de impresión por consola (`System.out.println`) dentro del constructor de `ProductoGeek` y otro mensaje distinto dentro del constructor de `VideojuegoFisico`. Es importante destacar que, por regla de Java, la llamada a `super()` debe ser siempre la primera instrucción dentro del constructor de la clase hija.

Dentro de la clase `Main`, implementé la lógica de prueba:
1. Instancié un único objeto de tipo `VideojuegoFisico` (Fatal Frame Maiden Of Black Water para Nintendo Switch).
2. Al ejecutar el programa, pude comprobar a través de la consola que, aunque yo instancié la clase hija, la JVM ejecutó primero el constructor de la clase padre (`ProductoGeek`) y recién después finalizó la ejecución del constructor de la clase hija (`VideojuegoFisico`). Esto demuestra cómo se forma la cadena de constructores de "arriba hacia abajo" en la jerarquía.

Ejecución en consola
<img width="1917" height="1018" alt="image" src="https://github.com/user-attachments/assets/5382d892-77da-4646-9713-117b18e7e4c3" />
