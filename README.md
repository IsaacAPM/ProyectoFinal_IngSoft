# Especificación de los Requerimientos del software
## Para 
# Aplicación de comunicación para miembros de la comunidad ITAM

### Hecho por 
- #### Anairam Mar Cuevas 181375
- #### Isaac Alejandro Pimentel Morales 184041 
- #### Carlos Andrés Ocampo Antonio 
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
El presente documento describe y plantea los requerimientos de software para el desarrollo de una aplicación de comunicación interna del Instituto Tecnológico Autónomo de México, con el objetivo de facilitar el intercambio de mensajes de texto, notas de voz y archivos entre alumnos, docentes y personal administrativo para solucionar dudas, entregar tareas y organizar grupos de trabajo y estudio. 

### Convención de documento

### Audiencia prevista
El presente documento está dirigido para la lectura y aprobación por parte del departamento de Servicios Escolares del ITAM, para el equipo de programadores que desarrollará la aplicación, para los "testers" o Quality Assurance Accountables que provarán las funcionalidades y remarcán los errores o bugs para su corrección, así como, para el Product Manager, con el objetivo de que coordine el proyecto ciñendose en este documento. 

### Sugerencias de lectura
Para su mejor lectura y comprensión, se sugiere leer el documento en orden secuencial y revisar la tabla de contenidos para localizar algún tema, funcionalidad o punto en específico. 

### Alcance del producto
La aplicación permitirá a los más de 4,000 alumnos, así como, a los profesores y personal administrativo comunicarse por mensajes de texto, notas de voz, vídeo y compartir archivos de manera ágil y agradable, pues su interfaz gráfica (UI) y las funcionalidades conformarán una buena experiencia de usuario (UX). 

### Referencias


## 2. Descripción general

### Perspectiva del producto
La aplicación tiene el objetivo de suplir y mejorar las necesidades de comunicación del ITAM que, actualmente, satisface el software Microsoft Teams. 
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

El usuario de tipo "Superusuario" tendrá las mismas funcionalidades que tienen los otros usuarios y, además, podrá enviar mensajes de difusión a todos los usuarios sin restricción, desactivar cuentas, crear y modificar los grupos de salones y equipos de trabajo administrativo. 

### Entorno operativo
La aplicación requerira un navegador web que soporte html5 y javascritp, preferentemente Google Chrome, FireFox o Microsoft Egde. 
### Limitaciones de diseño e implementación
La aplicación debera alojarse en los servidores del ITAM, por lo que esta limitada a la capacidad de estos. Ademas, la aplicación debera usar obligatoriamente el inico de sesión de microsoft.
### Documentación de usuario
### Dependencias y Supuestos
Se utilizara el API de inicio de sesión de microsoft.

## 3. Requisitos de la interfaz externa
### interfaz de usuario
### interfaz de hardware
### interfaz de software
### interfaz de comunicación
Se utilizaran los protocolos https, smtp. Se dede contratar un certificado de seguridad TLS.

## 4. Funcionalidades del sistema
### 4.1 Crear cuenta
#### 4.1.1 Descripción y prioridad
La prioridad es alta. Para que el usuario pueda utilizar el sistema de comunicación será necesario que cree una cuenta con sus datos, nombre de usuario y contraseña
#### 4.1.2 Secuencias de respuesta
El usuario ingresa a la página web, y presiona el botón de crear cuenta, se le pide su correo del ITAM y una contraseña además de algunos datos para completar su perfil
#### 4.1.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Que tenga capacidad para al menos 6,000  usuarios
Solo puede crear una cuenta con su correo del ITAM --> sino enviará una alterta de error con el mensaje "por favor ingrese su correo instucional"

### 4.2Inicio de sesión
#### 4.2.1 Descripción y prioridad
La prioridad es alta. Para inciar sesión el usuario escribe sus datos y entra al sistema.
#### 4.2.2 Secuencias de respuesta
El usuario entra en la página de inicio y hay dos botones iniciar sesión o crear cuenta, el usuario que ya tiene una cuenta da click en iniciar sesión por lo tanto necesitará escribir su nombre de usuario y contraseña, accede a la API de inicio de sesión de Microsoft verfica e ingresa.
#### 4.2.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Tener capacidad de al menos 6,000 usuarios.
Si el usuario ingresa datos incorrectos de tal forma que estos no se encuentran en la base de datos o no coinciden la aplicación enviara el mensaje "Datos incorrectos, por favor intentar de nuevo".

### 4.3 Ver lista de contactos ( barra de búsqueda)
#### 4.3.1 Descripción y prioridad
La prioridad es alta. Para poder establecer comunicación existe un apartado de contactos en donde estarán alumnos, profesores y administrtivos
#### 4.3.2 Secuencias de respuesta
El usuario se dirige al apartado de contactos donde encontrará una barra de búsqueda, ahí ingresará el nombre de la persona que busca. 
#### 4.3.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

### 4.4 Ver lista de conversaciones
#### 4.4.1 Descripción y calidad
La prioridad es alta. Habrá un apartado "chat" donde el usuario pordrá ver una lista de sus chats con el más reciente en la parte de arriba y así sucesivamente.
#### 4.4.2 Secuencias de respuesta
El usuario se dirige al apartado de "chat" ahí encontrará una lista de sus chats más recientes. Si quiere filtrar la búsqueda habrá un botón de filtrar, asimismo, podrá redactar un mensaje oprimiendo el botón de "nuevo chat"
#### 4.4.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Espacio suficiente para que 6000 usuarios puedan guardar sus chats

### 4.5 Enviar y recibir mensajes de texto
#### 4.5.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán enviar y recibir mensajes.
#### 4.5.2 Secuencias de respuesta
El usuario puede enviar mensajes utilizando diferentes botones que encontrará en la aplicación, oprime el botón y se abre una ventana de chat donde puede escribir el remitente y el mensaje. Para leer el mensaje el usuario se dirige a la ventana de chats donde tendrá una notificación abre el mensaje y lo lee.
#### 4.5.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

### 4.6 Enviar y recibir mensajes de voz
#### 4.6.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán enviar y recibir mensajes de voz.
#### 4.5.2 Secuencias de respuesta
l usuario puede enviar mensajes utilizando diferentes botones que encontrará en la aplicación, oprime el botón y se abre una ventana de chat donde puede escribir el remitente y grabar el mensaje de voz. Para escuchar el mensaje, el usuario se dirige a la ventana de chats donde tendrá una notificación abre el mensaje y lo escucha.
#### 4.5.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

### 4.7 Enviar y recibir archivos estáticos
#### 4.7.1 Descripción y prioridad
La prioridad es alta. Los usuarios podrán adjuntar archivos en sus mensajes y enviarlos.
#### 4.7.2 Secuencias de respuesta
El usuario abre la ventana de mensaje, oprime el botón de adjuntar archivo, selecciona el arhivo y lo adjunta. Adicionalmente, el usuario puede añadir un mensaje de texto o de voz al archivo que está enviando. Para recibir abre la ventana de chat que mostrará una notificación.
#### 4.7.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
Será necesario que pueda enviar documentos como pdf, jpg, doc y los tipos comunes de archivo.
Puede enviar 5 archivos máximo al mismo tiempo

### 4.8 Ver perfil propio y el de otros usuarios
#### 4.8.1 Descripción y prioridad
La prioridad es intermedia en este apartado el usuario podrá ver los datos de su propio perfil y también los de los otros usuarios con datos como nombre completo, correo del institucional, foto e intereses.
#### 4.8.2 Secuencias de respuesta
Para ver el propio perfil, el usuario se dirige al botón de "mis datos" y da click en ver perfil. Para ver el perfil de otros usuarios, el usuario va al apartado de contactos, busca a la persona y oprime el botón de ver perfil. 
#### 4.8.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
### 4.9 Editar el perfil propio
#### 4.9.1 Descripción y prioridad
La prioridad es intermedia. El usuario podrá editar datos de su perfil como intereses y foto.
#### 4.9.2 Secuencias de respuesta
El usuario da click en el botón de "mis datos" y luego en "modificar datos" y le aparecen los datos que puede modificar.
#### 4.9.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo.
### 4.10 Recibir notificaciones
#### 4.10.1 Descripción y prioridad
Prioridad alta. El usuario recibira notificaciones cuando le llegue un mensaje.
#### 4.10.2 Secuencias de respuesta
EL usuario recibe el mensaje y a la par una notificación de que ha recibido un mensaje.
#### 4.10.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo
### 4.11 Cerrar sesión
#### 4.11.1 Descripción y prioridad
Prioridad alta. El usuario cierra la sesión de su perfil por seguridad, de tal forma que sus datos queden seguros y nadie pueda mandar mensajes en su nombre.
#### 4.11.2 Secuencias de respuesta
El usuario va al botón de "mis datos" y luego al botón de "cerrar sesión".
#### 4.11.3 Requerimientos funcionales
Será necesario que la aplicación pueda procesar múltiples solicitudes al mismo tiempo

## 5. Otros requerimientos no funcionales
### Requerimientos de rendimiento
### Requerimientos de seguridad
### Atributos de calidad de software 
### Reglas de negocio

## 6. Otros Requerimientos

## Apendice A: Glosario
## Apendice B: Modelos de análisis









