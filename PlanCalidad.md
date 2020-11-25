# Plan de Calidad 
## Para 
# Aplicación de comunicación para miembros de la comunidad ITAM

### Hecho por 
- #### Anairam Mar Cuevas 181375
- #### Isaac Alejandro Pimentel Morales 184041 
- #### Carlos Andrés Ocampo Antonio 143599
- #### Diego Hernández Delgado 176262

### Instituto Tecnológico Autónomo de México
### 07 de noviembre de 2020

## Tabla de contenido
1) Test Plan Identifier 
2) Referencias 
3) Introducción 
4) Test Items 
5) Riesgos del Software  
6) Features por ser testeadas 
7) Features que no serán testeadas 
8) Approach  
9) Item Pass/Fail Criteria 
10) Suspension Criteria and Resumption Requirements 
11) Entregables 
12) Remaining Test Tasks 
13) Necesidades del ambiente 
14) Staffing and Training Needs 
15) Responsabilidades  
16) Agenda 
17) Planeación de riesgos y contingencias 
18) Approvals 
19) Glosario

## 1) Test Plan Identifier: 001-GW01
## 2) Referencias 

Tenemos el documento de Requerimientos del software
Las políticas de privacidad del ITAM y de los E. U. M.

## 3) Introducción 
Esto es un Test plan:
Se hará un testeo manual con métodos dinámicos.
Será un Black box Testing de funcionalidades y desempeño; ya que sólo requerimos probar la funcionalidad, pues todo lo relacionado con el diseño lo revisará el UX.

Se revisarán:
-Módulos
-Conexiones entre módulos
-Todo el sistema
-Acceptance testing

## 4) Test Items 
- Todas las paqueterías implementadas

## 5) Riesgos del Software 
- Que no pueda acceder a la apliación
- Que los mensajes no estén bien cifrados
- Que se sature el sistema
- Que los mensajes no lleguen a tiempo
- No poder asegurar la integridad de los mensajes
- Que se pueda robar la información

## 6) Features por ser testeadas 
- Crear cuenta
- Iniciar sesión con correo institucional
- Lista de contactos
- Enviar y recibir mensajes de texto
- Enviar y recibir mensajes de voz
- Enviar y recibir archivos estáticos
- Ver el perfil propio y el de otros usuarios
- Editar el perfil propio
- Recibir notificaciones

## 7) Features que no serán testeadas 
- Cerrar sesión
- Lista de conversaciones
- Buscador de conversaciones
- Buscador de contactos

## 8) Approach  
### Testing Levels
-Módulos
-Conexiones entre módulos
-Todo el sistema
-Acceptance testing
### Configuration Management/Change Control
Las personas que vayan a probar el sistema tienen que asegurarse entienda perfectamente la funcionalidad de cada módulo y de preferencia que sea el encargado de darle mantenimiento al sistema.

### Test Tools
*****

### Meetings
El día que se hagan las pruebas, se debe dar un reporte al encargado.

### Measures and Metrics
Se tiene que hacer una lista cuantitativa de:
  - El número de errores encontrados en cada módulo o sistema.
  -El valor de prueba:
  Nos referimos al valor de prueba con la siguiente métrica:
    -A cada error se le asignará un número de acuerdo al nivel de conflicto que genera:
      - Si el error es grave, es decir que pasme el sistema, se dará un valor de 10
      - Si el sistema no hace nada, es decir, que no cumple ninguna función,un valor de 9.
      - Si el error permite la funcionalidad pero no cumple su objetivo, un valor de 8.
      - Si el error hace que falle otro componente, valor de 7.
      - Si hay un fallo que pasa por alguna irresponsabilidad, un valor de 5.
      - Si no hay errores, valor de 0.
    
- Se considera que un sistema es óptimo entre menor sea el número de errores, es decir, mientras que el promedio se acerque a cero.
    
## 9) Item Pass/Fail Criteria 
Se considera que un componente, método o sistema pasa la prueba si y sólo cumple los requerimientos de los casos de uso sin que se presente algún error en su ejecución o en la interacción con otros sistemas y componentes.

Aunque el valor de prueba sea de 2 o menos, no se puede permitir que un sistema se considere aprobado si cuenta con al menos un componente que cause errores de valor 5 o superior.

## 10) Suspension Criteria and Resumption Requirements 
Si al momento de probar un componente o sistema se encuentran 2 errores de valor 10, se debe dejar de hacer la prueba y notificarle al PM a través de un reporte urgente para que tome las medidas necesarias.

Si el sistema o módulo logra un valor mayor a 5 se tomarán las medidas del caso previo.

Si el sistema o módulo (x) logra un valor: 2 < x < 5 se considera que el sistema tiene muchas fallas pero permiten la funcionalidad, se tienen que corregir.

Lo óptimo es que el sistema tenga un valor menor o igual a 2 para que se considere que fue probado con éxito.

## 11) Entregables 
El reporte debe ser un documento que contenga:
  - Día de testeo
  - Persona que hizo las pruebas
  - Funcionalidades probadas y que son correctas
  - Funcionalidades probadas incorrectas
    - Primero el número de prubas fallidas y a grosso modo el por qué se dieron las fallas
    - Detalle de cada una de las pruebas fallidas
    - Recomendaciones para solucionar los conflictos

Una vez entregado el reporte, el PM analizará y evaluará quién es la persona o personas idonesa para corregir los errores, entregará el reporte a los responsables.
Los responsables tendrán 3 hrs la borales para leer los casos y estimar el tiempo que se lleve a cabo los arreglos.

Se iterará cuantas veces sea necesario.

## 12) Remaining Test Tasks 
Tarea|Encargado|Estatus
------|------ | -------------
Acceptance Test Plan||
System/Integration Test Plan||
Unit Test rules and Procedures||
prototypes of Screens||

## 13) Necesidades del ambiente 
## 14) Staffing and Training Needs 
## 15) Responsabilidades 
## 16) Agenda 
## 17) Planeación de riesgos y contingencias  
## 18) Approvals 
## 19) Glosario
