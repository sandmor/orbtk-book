# Introducción

<!--
> WIP: para ser descomentado una vez que este listo
> Nota: Esta edición del libro es la misma que [The Orbital Widget Toolkit]
> [nsprust] disponible en formato impreso y como e-book en [No Starch Press][nsporbtk].

[nsporbtk]: https://nostarch.com/orbtk
[nsp]: https://nostarch.com/
-->

[<img src="img/orbtk.svg" width="720"/>](img/orbtk.svg)

Bienvenido a *The Orbital Widget Toolkit*, un libro introductorio acerca de `OrbTk`.
Rust como lenguaje de programación le ayuda a escribir código de forma más rápida y confiable.
`OrbTk` contribuye los _crates_ necesarios para desarrollar UIs modernas. Ofrece una misma base de código que puede compilar a código binario nativo para ejecutarse en la plataforma de su elección.

## Características

* API moderna y ligera
* Multiplataforma
* Crates modulares
* Basado en un Entity-Component-System(ECS) usando la libreria DCES
* Sistema de eventos flexible
* Libreria de widgets integrados
* Widgets personalizables
* Motor de temas personalizable
* Cambio de tema dinámico(en tiempo real)
* Herramientas de depuración integradas
* Localización

## Plataformas soportadas

* Redox OS (nativo)
* Linux (nativo | cargo-node)
* macOS (nativo | cargo-node)
* Windows (nativo | cargo-node)
* openBSD (no probado, pero debería trabajar)
* Web (cargo-node)
* Android (nativo planeado | cargo-node)
* iOS (nativo planeado | cargo-node planeado)
* Ubuntu Touch (nativo planeado | cargo-node planeado)

## Para quien es OrbTk

`OrbTk es ideal para programadores que les gusta tomar ventaja de las características que ofrece Rust. No hay necesida de transformar estructuras de datos o tipos: OrbTk en si mismo está escrito en Rust. Naturalmente adopta todas sus ventajas estructurales y provee los elementos gráficos necesarios para codificar tu aplicación. Tomemos una mirada de algunos de los más importantes grupos.

### Equipos de desarrolladores

Rust está probando ser una herramienta productiva para la colaboración entre grandes equipos de desarrolladores con variados niveles de conocimiento de programación de sistemas. Eche un vistazo al libro de Rust que elabora los principios fundamentales que le permiten producir un código más seguro.

`OrbTk` reutiliza la toolchain de Rust tanto como sea posible. El desarrollador contemporaneo que a pasado la curva de aprendizaje puede tomar ventaja de:

* Cargo, el manejador de dependencias y herramienta de compilación hace que añadir, compilar y manejar dependencias sea fácil y consistente a través de todo el ecosistema.
* Rustfmt asegura un estilo de código consistente entre múltiples desarrolladores.
* El servidor de lenguaje de Rust provee al IDE con autocompletado de código y mensajes de error a pie de código.

### Estudiantes

Rust es ideal para estudiantes y aquellos interesados en aprender acerca de los conceptos de la programación de sistemas. Usando Rust muchas personas han aprendido acerca de temas como por ejemplo el desarrollo de sistemas operativos. La comunidad es muy acogedora y feliz de responder a las preguntas de los estudiantes. A través de esfuerzos como este libro se busca hacer los conceptos de sistemas más accesibles a más personas, especialmente aquellas que son nuevas en la programación.

### Compañías

Cientos de compañías, grandes y pequeñas, usan Rust en producción para una variedad de tareas, ya sea herramientas de línea de comandos, servicios webs, herramientas de DevOps, sistemas embebidos, análisis de audio y video y transcodificación, criptomonedas, bioinformática, motores de búsqueda, internet de las cosas, machine learning e incluso partes considerables del navegador web Firefox.

### Desarrolladores de Open Source

`OrbTk` es para personas que quieren crear software con Rust, su comunidad, sus herramientas de desarrollo y librerías. Nos alegraría si contribuyeras a sus crates y entidades.

## Para quien es este libro

Este libro asume que as escrito código en algún lenguaje de programación y otros GUI toolkits, No hacemos ninguna suposición acerca de cuáles específicamente. Hemos intentado hacer este material ampliamente accesible a aquellos en una amplia variedad de trasfondos de desarrollo. No invertimos mucho tiempo en hablar acerca de que *es* programación o como pensar acerca de ella.
Si eres enteramente nuevo a la programación, estarás mejor asistido leyendo un libro que específicamente provee una introducción a la programación.

## Como usar este libro

En general, este libro asume que lo estás leyendo secuencialmente de adelante hacia atrás. Capítulos posteriores amplían conceptos explicados en capítulos anteriores, por lo tanto mientras que los primeros capítulos podrían no profundizar en los detalles de un tema específico; típicamente revisitamos dicho tema en los posteriores.

Encontrará dos tipos de capítulos en este libro: capítulos de conceptos y capítulos de proyecto. In los capítulos de concepto, aprenderá acerca de un aspecto de `OrbTk`. En capítulos de proyecto, construiremos pequeños programas juntos, aplicando lo que hallamos aprendido hasta el momento.

El capítulo 1 explica como instalar Rust y OrbTk, como escribir un programa minimo y como usar Cargo, el manejador de paquetes Rust y herramienta de compilación.

Finalmente, algunos apéndices contienen información útil. El apéndice A cubre las keywords de OrbTk y el B los traits derivables y crates.

No hay manera incorrecta de leer este libro: si quieres saltarte alguna parte hazlo!
Prodrías tener que mirar atrás a capítulos anteriores si experimentas alguna confusión, pero has lo que funcione para ti.

<span id="ferris"></span>

Una parte importante del proceso de aprender `OrbTk` es aprender como leer los mensajes de error que el compilador muestra: ellos te guiaran a hacer que tu código trabaje. Por lo tanto, proveeremos muchos ejemplos que no compilan junto con el mensaje de error que el compilador te mostrara en cada situación. Sea consciente de que si entra y ejecuta un ejemplo al azar, podría no compilar. Asegúrate de leer por tanto el texto circundante para ver si el ejemplo que estás intentando correr esta destinado a fallar. Ferris también te ayudará a distinguir código que está destinado a no funcionar:

| Ferris                                                                 | Significado                                            |
|------------------------------------------------------------------------|--------------------------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain"/>    | ¡Este código no compila!                               |
| <img src="img/ferris/panics.svg" class="ferris-explain"/>              | ¡Este código presenta un error fatal!                  |
| <img src="img/ferris/unsafe.svg" class="ferris-explain"/>              | Este bloque de código contiene código inseguro.        |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain"/>| Este bloque de código no produce el resultado deseado. |

En la mayoría de las situaciones, te llevaremos a la versión correcta de cualquier pieza de código que no compile.

## Código fuente

Los archivos del código fuente de los cuales este libro es generado pueden ser encontrados en  [Orbtk book (es)][orbtk_book_es].

[orbtk_book_es]: https://github.com/redox-os/orbtk-book/src/es

<!---
[orbtk_book_es]: https://www.redox-os.org/orbtk-book/book/en
[book]: https://github.com/redox-os/orbtk-bok
[book]: https://github.com/redox-os/orbtk/book/tree/master/src
-->
