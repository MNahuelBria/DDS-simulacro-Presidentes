# DDS-simulacro-Presidentes
##Instrucciones
1.Descargar el archivo RecParcial_DDS.zip (adjunto más abajo) 
2.Descomprimir el archivo RecParcial_DDS_3K6a.zip en la carpeta seleccionada para realizar el parcial
3.Programar la funcionalidad descrita más adelante con el título Consigna.
Importante: debe instalar las librerías dependientes del back y del front: 
Ejecutar el comando  npm install en ambos proyectos (en misma ruta donde está el archivo package.json).
4.Al finalizar el desarrollo, generar un unico archivo zip que contenga las carpetas backend y el fronted, excluyendo las carpetas node_modules de ambos proyectos. 
El archivo zip tiene que nombrarse con el siguiente patrón: `<apellido>_<nombre>_<legajo>.zip`
Por ejemplo, si te llamás `Juan Garcia Saravia` y tu legajo es `45044`, el archivo que debés subir será: `garcia_saravia_juan_45044.zip
Este zip generado debe se entregado como respuesta de esta tarea.

##Consigna:
Desarrollar el backend en el port 4000 y el frontend en el port 3000.
Desarrollo del  backend:  Se deberá agregar una funcionalidad de consulta para el nuevo recurso “Presidentes”:
El codigo para generar la taba en la base de datos ya se encuentra desarrollado en el archivo sqlite-init.js
Crear el modelo de sequelize que mapee la tabla Presidentes, acorde a la estructura descripta en el punto anterior.
Programar una ruta webapi con las siguientes características:

Un router para el endpoint “presidentes” que mediante el verbo/método GET  reciba un  parámetro:  “Nombre” y utilizando el ORM del punto anterior, recupere los registros filtrando por el parámetro recibido.  Deberá devolver todos los registros en cuyo campo “Nombre” contenga el valor del parámetro recibido. Devolver todos los campos de la tabla.
La aplicación deberá registrar como middleware el router con la ruta “/api/presidentes”. 
Asegure la funcionalidad probando las siguientes url desde el browser:

http://localhost:4000/api/presidentes
Debe devolver todos los registros.

http://localhost:4000/api/presidentes?Nombre=M
Debe devolver los registros que contengan “M” en el Nombre


Desarrollo del  frontend:  Se deberá agregar una interface de consulta para el recurso “presidentes” desarrollado en el backend

Desarrollar los componentes con el siguiente esquema:



Agregar el código necesario para poder realizar la consulta de presidentes. Se deberá realizar los componentes de react y consumir el backend desarrollado en el punto anterior.

En el componente Presidentes, incluir la interface de búsqueda con el campo a filtrar (“Nombre”) y el botón buscar.

Deberá consumir vía axios/fetch el endpoint del back.

En el componente PresidentesListado incluir una tabla de html para mostrar los resultados de la búsqueda, incluya en la misma todos los campos. (no se pide paginación). Los resultados deben estar ordenados por el contenido del campo “Nombre”

 

Agregar al componente menú de la aplicación, el acceso al nuevo componente.
