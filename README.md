# Especificación de los Requerimientos del software
## Para 
# Aplicación de comunicación para miembros de la comunidad ITAM
# Version 1.0

### Elaborado por 
- #### Anairam Mar Cuevas 181375
- #### Isaac Alejandro Pimentel Morales 184041 
- #### Carlos Andrés Ocampo Antonio 143599
- #### Diego Hernández Delgado 176262

### Instituto Tecnológico Autónomo de México
### 07 de noviembre de 2020

## Tabla de contenido

### Tabla de contenido
### Revisión de historia
1. Introducción
Objetivo 
Convención de documento
Audiencia prevista y sugerencias de lectura
Alcance del producto
Referencias

2. Descripción general
Perspectiva del producto
Funciones del producto
Clases de usuario y características
Entorno operativo
Limitaciones de diseño e implementación
Documentación de usuario
Dependencias y Supuestos

3. Requisitos de la interfaz externa
interfaz de usuario
interfaz de hardware
interfaz de software
interfaz de comunicación

4. Funcionalidades del sistema
Crear cuenta
Inicio de sesión
Ver lista de contactos ( barra de búsqueda)
Seleccionar método de comunicación
Chat individual
Videollamada
Grupo de conversación
Ver perfil
Modificar perfil
Notificaciones
Cerrar sesión

5. Otros requerimientos no funcionales
Requerimientos de rendimiento
Requerimientos de seguridad
Atributos de calidad de software 
Reglas de negocio

6. Otros Requerimientos

Apendice A: Glosario
Apendice B: Modelos de análisis


## 1. Introducción

### Objetivo 
El presente documento describe y plantea los requerimientos de *software* para el desarrollo de una aplicación de comunicación interna del Instituto Tecnológico Autónomo de México, con el objetivo de facilitar el intercambio de mensajes de texto, notas de voz y archivos entre alumnos, docentes y personal administrativo para solucionar dudas, entregar tareas y organizar grupos de trabajo y estudio. 

### Convención de documento
Las palabras anglosajonas propias de la jerga de tecnología, diseño o negocios tendrán un estilo de fuente itálica.
Cada requisito tendrá su orden de prioridad de desarrollo indicado del 1 al 5, de tal suerte que el 1 corresponde a la mayor prioridad y el 5 a la menor prioridad. En caso de que un requisito sea herencia o parte de otro más grande será indicado respectivamente. 

### Audiencia prevista
El presente documento está dirigido para la lectura y aprobación por parte del departamento de Servicios Escolares del ITAM, para el equipo de programadores que desarrollará la aplicación, para los "testers" o *Quality Assurance Accountables* que provarán las funcionalidades y remarcán los errores o *bugs* para su corrección y para el *Product Manager*, con el objetivo de que coordine el proyecto ciñéndose a este documento. 

### Sugerencias de lectura
Es recomendable leer este documento en orden secuencial o cronológico, es decir, de arriba a abajo, de derecha a izquierda, pues esta lectura permitirá una mejor comprensión de todos los requerimientos. Sin embargo, si se desea leer algún tema en particular, la tabla de contenidos o índice facilita la rápida ubicación del tema deseado como las especificaciones de algún módulo o funcionalidad. 

### Alcance del producto
La aplicación permitirá a los más de 4,000 alumnos, así como, a los profesores y personal administrativo comunicarse por mensajes de texto, notas de voz, vídeo y compartir archivos de manera ágil y agradable, pues su interfaz gráfica (UI) y las funcionalidades conformarán una buena experiencia de usuario (UX). 

### Referencias
- [Prototipo semifuncional](https://www.figma.com/proto/VoahKL2FrX9k4NXvX5IdEy/ITAM-CHAT-APP?node-id=4%3A6&scaling=min-zoom)
- El trabajo se basa en el material aprendido durante la materia de Ingeniería de Software, impartida por la profesora Paulina Bustos Arellano, quien, a través de distintas fuentes de consulta preparó cada viernes la clase y presentó las metodologías, técnicas y herramientas necesarias para llevar a cabo este proyecto, es por eso que ella funge como un contacto de referencia para resolver dudas y complementar el desarrollo deseado. 

## 2. Descripción general

### Perspectiva del producto
La aplicación tiene el objetivo de crear un canal institucional de comunicación para la comunidad ITAM que, actualmente, satisface el software Microsoft Teams. 
Esta aplicación formará parte del conjunto de servicios digitales que ofrece la universidad (Comunidad ITAM, Canvas, Servicios Personalizados-Grace).

### Funciones del producto
- Crear cuenta
- Iniciar sesión con correo institucional
- Lista de contactos
- Buscador de contactos
- Lista de conversaciones
- Buscador de conversaciones
- Enviar y recibir mensajes de texto
- Enviar y recibir mensajes de voz
- Enviar y recibir archivos estáticos 
- Ver el perfil propio y el de otros usuarios
- Editar el perfil propio
- Recibir notificaciones
- Cerrar sesión

### Clases de usuario y características
El usuario será diferenciado a través de una etiqueta en el perfil de usuario. Todos los usuarios tendrán una funcionalidad y privilegios similares con algunas diferencias que se mencionan a continuación.  

El usuario de tipo "Alumno" podrá tener acceso y capacidad para llevar a cabo todas las funcionalidades mencionadas en el apartado anterior (Funciones del producto).

Los usuarios de tipo "Maestro" y "Administrativo" tendrán las mismas funcionalidades que los usuarios de tipo "Alumno" y, además, podrán enviar mensajes de difusión. El tipo "Maestro" podrá enviar mensajes de difusión, únicamente, a todos los alumnos inscritos en sus grupos y el tipo "Administrativo" podrá enviar mensajes de difusión, únicamente, a todos los miembros de su departamento académico y/o administrativo. 

El usuario de tipo "Superusuario" tendrá las mismas funcionalidades que tienen los otros usuarios y, además, podrá enviar mensajes de difusión a todos los usuarios sin restricción. Aunque los grupos, se asignan automáticamente de acuerdo al registro de servicios académicos, habrá alguien con la capacidad de desactivar cuentas, crear y modificar los grupos de salones y equipos de trabajo administrativo. 

### Entorno operativo
-La aplicación requerirá de un navegador web que soporte HTML5 y JavaScrptp; preferentemente, Google Chrome, FireFox o Microsoft Egde. 
-Políticas corporativas o regulatorias.
-Las marcadas por el ITAM, el Estado Federal y de la Ciudad de México en relación a la privacidad de datos y manejo de información.

### Limitaciones de diseño e implementación
La aplicación deberá alojarse en los servidores del ITAM, por lo que está limitada a la capacidad de estos. Ademas, la aplicación deberá usar, obligatoriamente, el inico de sesión de Microsoft.

Será una plataforma pequeña para no más de 7 mil estudiantes, mil académicos y cien administrativos.

No se adquirirá ninguna plataforma nueva de soporte para la aplicación, todo se desarrollará con base en las limitaciones técnicas de la institución.
- Tecnologías:
  Node.js Runtime
  Express JS Framework 
  Angular Framework 
  MySQL

-Requisitos de idioma:
La interfaz de usuario estará disponible español e inglés.
Particularmente, la interfaz del superusuario y administradores estará en español.

- Consideraciones de Seguridad:
Guardar los hashes de las contraseña y no la contraseña normal.
Mantener la confidencialidad de la información. 
Garantizar la integridad de la información y su disponibilidad.

- Convenciones de diseño:
Seguir las convenciones de otras aplicaciones del ITAM, los colores de la institución así como logos y fuentes.

- Estándares de programación:
Se seguirán las convenciones de código de C#  de la Guía de programación de C#, que se pueden seguir en la página:
 https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/inside-a-program/coding-conventions
### Documentación de usuario
Haremos un manual para alumnos, otro para profesores, uno para administrativos, para el superuruario y uno final para los que se encarguen del mantenimiento de la plataforma.
Todo será escrito y compartido por medios institucionales, si las autoridades lo requieren haremos unos videotutoriales o daremos algunos talleres al momento de implementarlo.

### Dependencias y Supuestos
Como ya se mencionó, nos limitaremos a las características de los componentes y software y hardware que el ITAM ya maneja. Debido al enfoque institucional y académico del ITAM sólo se utilizara el API de inicio de sesión de microsoft. Respecto a reutilizar componentes del software se retomará solamente el concepto y los datos estrictamente necesarios.

## 3. Requisitos de la interfaz externa
### Interfaz de usuario

![Imgur](https://i.imgur.com/mFyzYpx.jpg)
![Imgur](https://i.imgur.com/eLg0dDo.jpg)
![Imgur](https://i.imgur.com/mhc1Atr.jpg)

### Interfaz de hardware
El servidor dedicado propiedad del ITAM tiene un sistema operativo Linux y un servidor Node.js con framework Express.js.

Del lado del cliente, como la aplicación será una plataforma web y una aplicación móvil, los requerimientos de software son muy amplios, pues cualquier dispositivo con un explorador web, un dispositivo Android y IOS podrá utilizar la aplicación, siempre y cuando esté conectada a internet.

### Interfaz de software

La plataforma será desarrollada en el lenguaje de programación TypeScript: particularmente, el desarrollo del backend que permitirá la lógica del servidor será desarrollado en el ambiente de ejecución Node.js y utilizará el framework Express.js para un manejo más agradable de la interacción HTTP. 

Por otro lado, se utilizará el framework Angular JS para desarrollar de manera ágil el código del Frontend y, si el cliente lo desea, se puede utilizar el framework Ionic para generar código híbrido que corra en dispositivos móviles iOS y Android.
Por su robustez, el manejador de base de datos (DBMS) a utilizar será MySQL.

Para la seguridad de la conexión del protocolo HTTPS se comparará un certificado de seguridad TLS de la compañía GTS CA 1O1. 

Para verificar los usuarios, utilizaremos un microservicio de Microsoft Outlook para mantener una relación de nuestra base de datos con los correos institucionales. 

Para el proceso de desarrollo, utilizaremos Visual Studio Code como editor de código, Git y GitHub para la gestión de versiones y compartir el código.

### Interfaz de comunicación
Se utilizaran los protocolos https, smtp. Se dede contratar un certificado de seguridad TLS.

## 4. Funcionalidades del sistema
4.1 Crear cuenta
4.2 Iniciar sesión con correo institucional
4.3 Lista de contactos
4.4 Buscador de contactos
4.5 Lista de conversaciones
4.6 Buscador de conversaciones
4.7 Enviar y recibir mensajes de texto
4.8 Enviar y recibir mensajes de voz
4.9 Enviar y recibir archivos estáticos 
4.10 Ver el perfil propio y el de otros usuarios
4.11 Editar el perfil propio
4.12 Recibir notificaciones
4.13 Cerrar sesión

### 4.1 Crear cuenta
#### 4.1.1 Descripción y prioridad
La prioridad es alta. Para que el usuario pueda utilizar el sistema de comunicación será necesario que cree una cuenta con sus datos: correo electrónico institucional y contraseña del mismo.
#### 4.1.2 Secuencias de respuesta
El usuario ingresa a la página principal, y presiona el botón de  *Log-In*. Posteriormente, se le muestra una pantalla donde podrá y deberá ingresar su correo del ITAM y una contraseña. En el caso de que la autenticación del correo con el microservicio de Microsoft sea exitosa, se le redigirá a la pantalla del *chat*, en caso contrario, se le mostrará un mensaje de error. 
Aunque el flujo de pantallas y la experiencia de usuario es identica para quien ingresa por primera vez como para quien ingresa recurrentemente, en el proceso del backend, hay una radical diferencia, pues cuando es la primera vez, se obtienen los datos de la cuenta de correo y se registran en la base de datos del presente sistema. 
#### 4.1.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo.
Que tenga capacidad para al menos 6,000  usuarios.
Solo puede crear una cuenta con su correo del ITAM, de lo contrario, se desplegará la pantalla de error que le dará la opción de "Ir a Microsoft" para solucionar los problemas de contraseña o el botón de "Intentar de nuevo" para hacer lo propio. 

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/1.-Landing.png "1.-Landing.png")
![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/2.-Log-In.png "2.-Log-In.png")

### 4.2Inicio de sesión con correo institucional
#### 4.2.1 Descripción y prioridad
La prioridad es alta. Para inciar sesión el usuario escribe sus datos y entra al sistema.
#### 4.2.2 Secuencias de respuesta
El usuario ingresa a la página principal, y presiona el botón de  *Log-In*. Posteriormente, se le muestra una pantalla donde podrá y deberá ingresar su correo del ITAM y una contraseña. En el caso de que la autenticación del correo con el microservicio de Microsoft sea exitosa, se le redigirá a la pantalla del *chat*, en caso contrario, se le mostrará un mensaje de error. 
Aunque el flujo de pantallas y la experiencia de usuario es identica para quien ingresa por primera vez como para quien ingresa recurrentemente, en el proceso del backend, hay una radical diferencia, pues cuando es la primera vez, se obtienen los datos de la cuenta de correo y se registran en la base de datos del presente sistema. 
#### 4.2.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Tener capacidad de al menos 6,000 usuarios.
Si el usuario ingresa datos incorrectos de tal forma que estos no se encuentran en la base de datos o no coinciden la aplicación enviara el mensaje "Datos incorrectos, por favor intentar de nuevo".

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/2.-Log-In.png "2.-Log-In.png")


### 4.3 Ver lista de contactos (barra de búsqueda)
#### 4.3.1 Descripción y prioridad
La prioridad es alta. Para poder establecer comunicación existe un apartado de contactos en donde estarán alumnos, profesores y administrtivos.
En la visualización de la lista, se podrá apreciar la imagen de perfil, un círculo sobre la imagen de perfil para indicar si está en línea (verde y rojo), el nombre de usuario y un ícono representativo del tipo de usuario y(estudiante, administrativo, maestro); en el caso que ya se haya iniciado una conversación con anterioridad, se mostrará el número de mensajes no leídos. 
#### 4.3.2 Secuencias de respuesta
El usuario se dirige al apartado de contactos donde encontrará una barra de búsqueda, ahí ingresará el nombre de la persona que busca. 
#### 4.3.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo. Las búsquedas se realizarán con todos los usuarios que ya estén registrados en la plataforma, sin importar si aún no han iniciado una conversación ni el tipo de usuario. 

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/7.-ContactosYBarraDeBúsqueda.png "7.-ContactosYBarraDeBúsqueda.png")

### 4.4 Ver lista de conversaciones
#### 4.4.1 Descripción y calidad
La prioridad es alta. Habrá un apartado "chat" donde el usuario pordrá ver una lista de sus chats con el más reciente en la parte de arriba y así sucesivamente.
#### 4.4.2 Secuencias de respuesta
El usuario se dirige al apartado de "chat" ahí encontrará una lista de sus chats más recientes. Si quiere filtrar la búsqueda habrá un botón de filtrar, asimismo, podrá redactar un mensaje oprimiendo el botón de "nuevo chat".
En la visualización de la lista, se podrá apreciar la imagen de perfil, un círculo sobre la imagen de perfil para indicar si está en línea (verde y rojo), el nombre de usuario y un ícono representativo del tipo de usuario y(estudiante, administrativo, maestro); en el caso que ya se haya iniciado una conversación con anterioridad, se mostrará el número de mensajes no leídos y la última vez que estuvo activo. 
#### 4.4.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Espacio suficiente para que 6000 usuarios puedan guardar sus chats

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/6.-ListadeChat.png "6.-ListadeChat.png")


### 4.5 Enviar y recibir mensajes de texto
#### 4.5.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán enviar y recibir mensajes.
#### 4.5.2 Secuencias de respuesta
El usuario puede enviar mensajes utilizando diferentes botones que encontrará en la aplicación, oprime el botón y se abre una ventana de chat donde puede escribir el remitente y el mensaje. Para leer el mensaje el usuario se dirige a la ventana de chats donde tendrá una notificación, abre el mensaje y lo lee.
En la ventana de chat, se podrán leer los mensajes de los otros usuarios del lado izquierdo en color azul, con la imagen de perfil a un lado de cada uno, así como, la hora de envío. De manera similar, pero del otro lado (derecho) se mostrarán los mensajes enviados por el usuario en primera persona con las características anteriores. 
#### 4.5.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/5.-ChattApp.png "5.-ChattApp.png")


### 4.6 Enviar y recibir mensajes de voz
#### 4.6.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán enviar y recibir mensajes de voz.
#### 4.5.2 Secuencias de respuesta
El usuario puede enviar mensajes utilizando diferentes botones que encontrará en la aplicación, oprime el botón y se abre una ventana de chat donde puede escribir el remitente y grabar el mensaje de voz. Para escuchar el mensaje, el usuario se dirige a la ventana de chats donde tendrá una notificación abre el mensaje y lo escucha.
#### 4.5.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/8.-Envío_de_mensajes.png "8.-Envío_de_mensajes.png")


### 4.7 Enviar y recibir archivos estáticos
#### 4.7.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán adjuntar archivos en sus mensajes y enviarlos.
#### 4.7.2 Secuencias de respuesta
El usuario abre la ventana de mensaje, oprime el botón de adjuntar archivo, selecciona el arhivo y lo adjunta. Adicionalmente, el usuario puede añadir un mensaje de texto o de voz al archivo que está enviando. Para recibir abre la ventana de chat que mostrará una notificación.
#### 4.7.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Será necesario que pueda enviar documentos como pdf, jpg, doc y los tipos comunes de archivo.
Puede enviar 5 archivos máximo al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/8.-Envío_de_mensajes.png "8.-Envío_de_mensajes.png")


### 4.8 Ver perfil propio y el de otros usuarios
#### 4.8.1 Descripción y prioridad
La prioridad es intermedia en este apartado el usuario podrá ver los datos de su propio perfil y también los de los otros usuarios con datos como nombre completo, correo del institucional, foto e intereses.
#### 4.8.2 Secuencias de respuesta
Para ver el propio perfil, el usuario se dirige al botón de "mis datos" y da click en ver perfil, dicho botón se representa por unícono de tres puntos verticales a un lado del nombre del perfil propio, es decir, en la patrte superior derecha de toda la pantalla de chat. Para ver el perfil de otros usuarios, el usuario va al apartado de contactos, busca a la persona, abre el chat, da click en el ícono de los tres puntos verticales que se encuentran en la parte superior derecha y oprime el botón de ver perfil.
#### 4.8.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/7.-ContactosYBarraDeBúsqueda.png "Imagen: ver perfil propio y el de otros usuarios")

### 4.9 Editar el perfil propio
#### 4.9.1 Descripción y prioridad
La prioridad es intermedia. El usuario podrá editar datos de su perfil como intereses y foto.
#### 4.9.2 Secuencias de respuesta
El usuario da click en el botón de "mis datos" y luego en "modificar datos" y le aparecen los datos que puede modificar.
#### 4.9.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo.

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/9.-Menú_para_sali_de_sesión.png "Imagen: editar el perfil propio")

### 4.10 Recibir notificaciones
#### 4.10.1 Descripción y prioridad
Prioridad alta. El usuario recibira notificaciones cuando le llegue un mensaje.
#### 4.10.2 Secuencias de respuesta
EL usuario recibe el mensaje de algún contacto y esa conversación se coloca en la primera posición de la lista de chats con un pequeña círculo que indica la cantidad de mensajes no leídos. 
#### 4.10.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/6.-ListadeChat.png "6.-ListadeChat.png")

### 4.11 Cerrar sesión
#### 4.11.1 Descripción y prioridad
Prioridad alta. El usuario cierra la sesión de su perfil por seguridad, de tal forma que sus datos queden seguros y nadie pueda mandar mensajes en su nombre.
#### 4.11.2 Secuencias de respuesta
El usuario va al botón de "mis datos" y luego al botón de "cerrar sesión".
#### 4.11.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/9.-Menú_para_sali_de_sesión.png "Imagen: editar el perfil propio")


## 5. Otros requerimientos no funcionales
### Requerimientos de rendimiento
Debe existir un balanceo de cargas, así como, un firewall que ayude a detener ataques DDOS.

### Requerimientos de seguridad
Es necesario que el usuario no comparta sus datos de acceso (usuario y contraseña) para mantener seguro el sistema de cambios indeseados, no obstante, se cuenta con acceso al sistema para hacer cambios arbitrarios por parte de las autoridades pertinentes si es necesario hacer modificaciones sobre acciones previamente realizadas o modificaciones independientes que quieran realizarse. Se recomienda leer el manual antes de realizar la inscripción o baja para asegurar que el usuario pueda realizar las acciones deseadas sobre todo porque las inscripciones suelen ser rápidas debido a que los grupos más cotizados se llenan rápido (no se recomienda que el alumno llegue a su inscripción a aprender como inscribirse). Asimismo, es importante que los administradores lean también el manual para que sepan realizar sus acciones y puedan resolver los asuntos escolares. De haber un error con el sistema se deberá llamar a la oficina de inscripciones para recibir apoyo y analizar el caso.

Será necesario proteger los servidores donde se almacenarán los datos de los alumnos, así como proteger la página de posible robo de contraseñas. Para cambiar la contraseña actual será necesario ingresar la contraseña anterior y de olvidar la contraseña se le enviará un correo al usuario para garantizar que no se trata de otra persona.


### Atributos de calidad de software 
Como se utilizará el framework Angular JS para desarrollar de manera ágil el código del Frontend, si el cliente lo desea más, se puede utilizar el framework Ionic para generar código híbrido que corra en dispositivos móviles iOS y *Android*.
Por su robustez, el manejador de base de datos (DBMS) a utilizar será *MySQL*.

### Reglas de negocio
El usuario alumno podrá ingresar, ver su horario, buscar alumnos, maestros y administrativos. 
El usuario profesor, podrá hacer lo mismo pero con la oportunidad de crear listas de difusión. 
El superusuario es aquel que el ITAM designa para hacer las correcciones manualmente y de forma pertinente, de los errores que el sistema haya cometido o que se quieran hacer directamente.

Se sugiere que haya un superusuario por cada departamento académico.

## 6. Otros Requerimientos
Es fundamental basarse en el Aviso de Privacidad y Términos y Condiciones ordinario del ITAM para que todos los datos de los usuarios sean protegidos como se indican y cualquier usuario tenga conocimiento de esto.

## Apéndice A: Glosario
HTTP: Hyper Text Transfer Protocol

HTTPS: Hyper Text Transfer Protocol Secure

API: Aplication Protocol Interface

Servidor: computadora o conjunto de computadoras dedicadas a responder a una arquitectura de Cliente-Servidor

Cliente: dispositivo móvil o computadora que solicita información al servidor. 

Microservicio: tipo de arquitectura de software que utiliza Restful API’s.

## Apéndice B: Modelos de análisis

### Ejemplo de arquitectura del software de una aplicación de chat genérica

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/10.-Ejemplo_de_Arquitectura_de_CatApp.png "Imagen: Ejemplo_de_Arquitectura_de_CatApp")

[Fuente](https://medium.com/@sudarakayasindu/behind-the-scenes-of-chat-applications-38634f584758)

### Ejemplo de esquema de base de datos de una aplicación de chat genérica

![alt text](https://github.com/IsaacAPM/ProyectoFinal_IngSoft/blob/main/8.-Im%C3%A1genes/11.-Ejemplo_Esquema_BD_ChatApp.png "Imagen: Ejemplo_Esquema_BD_ChatApp")

[Fuente](https://stackoverflow.com/questions/46484989/database-schema-for-chat-private-and-group)






