**Flores Alvarado Julio Cesar**

**Ensayo de un Modelo-Vista-Controlador**

**Instituto Tecnológico de Tláhuac**

**Ingeniería en Sistemas Computacionales**

**Grupo: 8S2. Programación Web PHP con MVC**

**21 de marzo de 2024**

<hr>
</hr>

**Índice**

***Resumen		1***

***Introducción	1***

***Desarrollo	1***

***Conclusiones	12***

***Referencias	13***

<hr>
</hr>

***Resumen***

*El Modelo-Vista-Controlador (MVC) es un patrón arquitectónico ampliamente utilizado en el desarrollo de software. Este enfoque divide una aplicación en tres componentes principales: el modelo, que representa los datos y la lógica de negocio; la vista, que se encarga de la presentación de la información al usuario; y el controlador, que actúa como intermediario entre el modelo y la vista. Este ensayo explora la importancia del MVC en el desarrollo de software moderno, sus beneficios y su aplicación en diferentes contextos.*

<hr>
::before
::after
</hr>

***Introducción***
*En el panorama actual del desarrollo de software, el modularidad, la escalabilidad y la mantenibilidad son aspectos cruciales para el éxito de un proyecto. El patrón MVC surge como una solución elegante para abordar estos desafíos al promover la separación de preocupaciones y la organización estructurada del código. Al dividir una aplicación en tres componentes distintos pero interconectados, MVC permite un desarrollo más ordenado, facilita la reutilización de código y promueve una mayor flexibilidad y adaptabilidad a medida que los requerimientos evolucionan.*

<hr>
</hr>

***Desarrollo***
Estos archivos son utilizados para crear una página web con funcionalidades básicas como la estructura de la cuadrícula, botones, formularios, barras de desplazamiento, alertas, ventanas emergentes y más. También se utilizan para aplicar estilos a la página web y mejorar la experiencia del usuario.

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 001](https://github.com/JulioFlores24/Prestamos2/assets/168167417/85b9bcfd-c69c-44a6-83cf-133edf34c013)

El Modelo-Vista-Controlador se compone de tres elementos clave:

***Modelo:***

*El modelo representa los datos subyacentes de la aplicación y la lógica de negocio asociada. Es responsable de manejar la manipulación y el almacenamiento de los datos, así como de aplicar las reglas de negocio necesarias para procesarlos correctamente. Al separar la lógica de negocio del resto de la aplicación, el modelo facilita la reutilización y la prueba de la funcionalidad de manera independiente.*

**LoginModelo.php**

Define una clase loginModelo que extiende otra clase llamada mainModel, indicando que probablemente herede funcionalidades relacionadas con la interacción con la base de datos. Dentro de esta clase, hay un método protegido llamado iniciar\_sesion\_modelo($datos), que se encarga de iniciar sesión en el sistema. Este método ejecuta una consulta SQL preparada para seleccionar los datos de usuario correspondientes a las credenciales proporcionadas. El resultado de la consulta se devuelve para su posterior procesamiento, como verificar si las credenciales son válidas.

**mainModel.php**

Esta clase proporciona una serie de funciones esenciales para realizar operaciones comunes en un sistema, como interactuar con la base de datos, validar datos, encriptar y desencriptar información, y gestionar la paginación de resultados. Esto promueve la reutilización de código y la implementación eficiente de funcionalidades en el sistema.

**usuarioModelo.php**

Estos métodos ofrecen una interfaz para realizar operaciones comunes de CRUD (Crear, Leer, Actualizar, Eliminar) en la tabla de usuarios, promoviendo la modularidad y reutilización del código.

**vistasModelo.php**

Este código determina la vista que se debe cargar en función de la solicitud del usuario, asegurando que solo se acceda a vistas permitidas y manejando adecuadamente los casos donde la vista solicitada no existe.

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 002](https://github.com/JulioFlores24/Prestamos2/assets/168167417/662cf07c-d7cf-4969-8849-8d7e4036b204)

***Vista:***

*La vista es la interfaz de usuario que presenta la información al usuario final de manera comprensible y atractiva. Su principal función es mostrar los datos proporcionados por el modelo y permitir la interacción del usuario con la aplicación. Al separar la lógica de presentación del resto del sistema, la vista facilita la adaptación a diferentes dispositivos y plataformas sin afectar la lógica subyacente.*

**Index.php**

*Este código PHP carga la configuración de la aplicación y el controlador de vistas, crea una instancia del controlador de vistas y llama a un método en ese controlador para obtener y renderizar la plantilla principal de la aplicación.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 003](https://github.com/JulioFlores24/Prestamos2/assets/168167417/2c0ec100-7c2d-476c-baa0-a5e46c892dd6)

**.htacces**

*Reescribe cualquier solicitud de URL que consista en letras, números, barras inclinadas, o los caracteres ñ, Ñ, o -, a index.php, pasando el valor capturado como un parámetro views. Por ejemplo, una solicitud a mi\_pagina se reescribiría internamente como index.php?views=mi\_pagina.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 004](https://github.com/JulioFlores24/Prestamos2/assets/168167417/e314b8ab-bc5a-4c8e-aa08-cb1cbcc881f5)

**Plantilla.php**

*Este código HTML con incrustaciones de PHP establece la estructura básica de una página web dinámica. Incluye un encabezado con metadatos y un título obtenido de una constante PHP. Se carga un archivo PHP para enlaces externos. El cuerpo del documento contiene lógica condicional en PHP para gestionar qué contenido mostrar, dependiendo de la solicitud. Se verifica la existencia de variables de sesión y se redirecciona al inicio de sesión si es necesario. La página principal incluye una barra lateral de navegación y el contenido principal se carga dinámicamente según la vista solicitada. Finalmente, se incluyen archivos PHP adicionales para manejar el cierre de sesión y se cargan scripts necesarios para la funcionalidad de la página.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 005](https://github.com/JulioFlores24/Prestamos2/assets/168167417/0b3abd2f-a92e-412b-9aba-1487aadc4a93)

**NavBar.php**

*Este código HTML representa una barra de navegación con tres enlaces. El primer enlace activa/desactiva una barra lateral de navegación. El segundo enlace lleva a una página de actualización de usuario, con la URL construida dinámicamente usando PHP para incluir el ID de sesión cifrado. El tercer enlace parece ser un botón de cierre de sesión.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 006](https://github.com/JulioFlores24/Prestamos2/assets/168167417/491511e1-35ca-4bfd-ad55-6be0ddfaef5f)

**NavLateral.php**

*Este bloque de código HTML con incrustaciones de PHP describe la estructura de una barra de navegación lateral utilizada en una aplicación web. Está compuesto por dos elementos principales dentro de un contenedor <section>. Primero, un fondo oscuro transparente que se muestra cuando la barra lateral está activa, y luego el contenido real de la barra lateral, que incluye un avatar de usuario, una barra de separación y un menú de navegación. Este menú de navegación contiene una lista de elementos de menú representados por enlaces, generados dinámicamente utilizando PHP para construir las URL. Algunos elementos de menú pueden estar condicionados según el nivel de privilegio del usuario, mostrando ciertas opciones de menú solo para usuarios con privilegios específicos.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 007](https://github.com/JulioFlores24/Prestamos2/assets/168167417/d4d71377-c628-4516-9e37-57d99a310504)

**Script.php**

*Describe la inclusión de varios archivos JavaScript en una página web. Los archivos incluidos son principalmente bibliotecas y scripts personalizados esenciales para la funcionalidad y el diseño de la página. Esto incluye bibliotecas como jQuery, Popper, Bootstrap, y Bootstrap Material Design, que proporcionan funcionalidades como manipulación del DOM, posicionamiento de elementos emergentes, estilos y componentes de interfaz de usuario. Además, se incluyen scripts personalizados como **main.js** y **alertas.js**, que pueden proporcionar funcionalidades específicas y personalizadas para la página web.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 008](https://github.com/JulioFlores24/Prestamos2/assets/168167417/9dbd8893-34ca-4c08-bba8-604c10304e21)

**LogOut.php**

*Este script implementa la funcionalidad de salida del sistema al hacer clic en un botón específico. Utiliza SweetAlert para mostrar un cuadro de diálogo de confirmación. Si el usuario confirma la salida, se envía una solicitud AJAX al servidor para cerrar la sesión del usuario actual. La solicitud incluye el token de sesión y el nombre de usuario cifrados para garantizar la seguridad de la operación. Una vez completada la solicitud, se procesa la respuesta del servidor, probablemente mostrando alertas o notificaciones al usuario. En resumen, este sistema proporciona una forma segura y controlada para que los usuarios salgan del sistema.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 009](https://github.com/JulioFlores24/Prestamos2/assets/168167417/6a6e4877-06d5-453a-bae7-8f2e97dc9f7f)

**Link.php**

*Describe la inclusión de varios archivos CSS y JavaScript en una página web. Los archivos incluidos proporcionan estilos y funcionalidades para la interfaz de usuario de la página. Esto incluye estilos de normalización (**normalize.css**), estilos y componentes de Bootstrap (**bootstrap.min.css**), estilos de diseño de material de Bootstrap (**bootstrap-material-design.min.css**), iconos de Font Awesome (**all.css**), estilos para alertas personalizadas (**sweetalert2.min.css**), y estilos para barras de desplazamiento personalizadas (**jquery.mCustomScrollbar.css**). Además, se incluye un archivo JavaScript para las alertas personalizadas (**sweetalert2.min.js**). Estos archivos ayudan a establecer la apariencia y el comportamiento deseado de la página web.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 010](https://github.com/JulioFlores24/Prestamos2/assets/168167417/48e9d7a8-36b2-41da-8df2-21b0da01b4bf)

*El sistema de préstamos cuenta con una serie de archivos de vista en el directorio "vistas". Cada archivo .php en este directorio representa una vista específica dentro del sistema, desde la visualización de clientes y ítems hasta la gestión de reservas y usuarios. Estas vistas proporcionan una interfaz para realizar diversas acciones, como agregar nuevos clientes o buscar ítems disponibles.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 011](https://github.com/JulioFlores24/Prestamos2/assets/168167417/26176bfe-f68e-477b-b487-5eb907e1be9b)

*Los archivos en la carpeta assets son esenciales para el funcionamiento del sistema de préstamos. Estos archivos proporcionan las imágenes, iconos, JavaScript, CSS y fuentes que se utilizan para crear una interfaz de usuario atractiva y funcional.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 012](https://github.com/JulioFlores24/Prestamos2/assets/168167417/639966d4-4095-4061-9cee-f3264bb4c943)

*Se muestra como se ve nuestro sistema de ventas ya ejecutándolo.*

**“Login”**

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 013](https://github.com/JulioFlores24/Prestamos2/assets/168167417/f05646ff-189a-4ad9-9336-892cf9c7ffce)

**"Sistema de préstamos**”

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 014](https://github.com/JulioFlores24/Prestamos2/assets/168167417/c53c759b-8490-4245-9295-5ed6c1412c12)

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 015](https://github.com/JulioFlores24/Prestamos2/assets/168167417/c3ff2a3b-9f37-437a-bb4f-0d7f405c261b)

**Controlador:**

*El controlador actúa como intermediario entre el modelo y la vista, gestionando las interacciones del usuario y actualizando el modelo en consecuencia. Se encarga de interpretar las acciones del usuario, invocar las operaciones adecuadas en el modelo y actualizar la vista correspondiente. Esta separación de responsabilidades permite una mayor flexibilidad en el manejo de eventos y una fácil integración de nuevas funcionalidades sin afectar la estructura existente.*

*La implementación del patrón MVC conlleva una serie de beneficios significativos para el desarrollo de software. Entre ellos se incluyen una mejor organización del código, una mayor modularidad y reutilización, una facilidad de mantenimiento y evolución, y una mayor escalabilidad y adaptabilidad a medida que los requisitos cambian.*

**loginControlador.php**

*Este controlador gestiona el inicio de sesión, el cierre de sesión y la forzada cierre de sesión del usuario en el sistema, garantizando la seguridad y la integridad de los datos del usuario.*

**usuarioControlador.php**

*El código PHP proporcionado define una clase llamada usuarioControlador que extiende la clase usuarioModelo. Esta clase contiene varios métodos para controlar las operaciones relacionadas con los usuarios en un sistema. Por ejemplo, el método agregar\_usuario\_controlador() valida y agrega un nuevo usuario a la base de datos, mientras que el método eliminar\_usuario\_controlador() gestiona la eliminación de usuarios. Otros métodos se encargan de actualizar los datos de un usuario, paginar la lista de usuarios y recuperar información específica de un usuario. El código también utiliza funciones de validación para garantizar la integridad de los datos antes de realizar operaciones en la base de datos, y utiliza JSON para manejar las respuestas y alertas del sistema de forma dinámica.*

**vistasControlador.php**

*Este código PHP define la clase **vistasControlador**, que extiende otra clase llamada **vistasModelo**. Dos métodos principales son definidos: **obtener\_plantilla\_controlador()** devuelve la ruta a la plantilla principal del sitio, mientras que **obtener\_vistas\_controlador()** determina qué vista cargar según la URL proporcionada. Si se especifica una vista en la URL, se obtiene utilizando el método correspondiente del modelo; de lo contrario, se carga la vista predeterminada "login".*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 016](https://github.com/JulioFlores24/Prestamos2/assets/168167417/a3d50dd5-0239-4613-8844-d20da4be6faf)

**Diagrama de casos de uso**

*Este diagrama de casos de uso muestra el modelo lógico de los datos de un sistema.*

![Aspose Words 9d310a66-e3c3-49fb-b132-20ea124bc805 017](https://github.com/JulioFlores24/Prestamos2/assets/168167417/8b204f1e-84a8-4813-aeb5-644425d6e54d)

<hr>
</hr>

**Conclusiones**

*En conclusión, el Modelo-Vista-Controlador es un enfoque fundamental en el desarrollo de software moderno. Al separar las preocupaciones de datos, presentación y control, MVC promueve una arquitectura más limpia, modular y fácil de mantener. Su adopción puede resultar en un código más robusto, escalable y flexible, lo que a su vez contribuye a la eficiencia y el éxito a largo plazo de los proyectos de software. Con su capacidad para adaptarse a una amplia gama de aplicaciones y contextos, el patrón MVC continúa siendo una herramienta invaluable para los desarrolladores en la creación de aplicaciones de alta calidad y rendimiento.*

<hr>
</hr>

**Referencias**

1. *Alvarez, M. A. (20 de Septiembre de 2023). *Desarrollo Web*. Recuperado el 19 de Marzo de 2024, de Qué es MVC: https://desarrolloweb.com/articulos/que-es-mvc.html*

2. *AppMaster. (07 de Septiembre de 2023). Recuperado el 19 de Marzo de 2024, de Modelo-Vista-Controlador (MVC): https://appmaster.io/es/glossary/modelo-vista-controlador-mvc-es*

4. *Developer Mozilla. (13 de Noviembre de 2023). Recuperado el 19 de Marzo de 2024, de MVC: https://developer.mozilla.org/es/docs/Glossary/MVC*

5. *Francisco J. Vera-Garcia, J. M. (1 de Febrero de 2010). *Journal of Electromyography and Kinesiology*. Recuperado el 19 de Marzo de 2024, de MVC techniques to normalize trunk muscle EMG in healthy women: https://www.sciencedirect.com/science/article/abs/pii/S1050641109000571*

7. *Hernández, U. (22 de Febrero de 2015). *Codigo Facilito*. Recuperado el 19 de Marzo de 2024, de MVC (Model, View, Controller) explicado: https://codigofacilito.com/articulos/mvc-model-view-controller-explicado*
