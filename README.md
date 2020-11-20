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

### Inicio de sesión
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

### Seleccionar método de comunicación
### Chat individual
### Videollamada
### Grupo de conversación
### Ver perfil
### Modificar perfil
### Notificaciones
### Cerrar sesión

## 5. Otros requerimientos no funcionales
### Requerimientos de rendimiento
### Requerimientos de seguridad
### Atributos de calidad de software 
### Reglas de negocio

## 6. Otros Requerimientos

## Apendice A: Glosario
## Apendice B: Modelos de análisis









