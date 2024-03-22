# Introducción a la Base de Datos con PostgreSQL.
<br> 

![postgres-logo](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/4dae2a3a-d48d-4c2c-9e46-24c3e548fa73)

## Descripción.

Introducción practica a PostgresSQL, al ser un sistema de gestión de Base de Datos relacional, se aprenderá desde 
la instalación y configuración del entorno hasta el modelado de los datos, consultas SQL y administración eficiente 
de Bases de Datos en entornos reales, en donde se tendrán en cuenta aspectos teóricos y prácticos relacionados con 
la seguridad y la integridad de los datos.

<br>

## ¿Que es y para que sirve PostgreSQL?

Es un motor de gestión de bases de datos relacional de código abierto y de alto rendimiento. Es conocido por su fiabilidad, robustez y capacidad para manejar grandes volúmenes de datos. PostgreSQL es altamente compatible con los estándares SQL y admite una amplia gama de tipos de datos, funciones y características avanzadas, lo que lo hace ideal para aplicaciones empresariales y proyectos en general.

Existen 3 conceptos en relación a las bases de datos.

1. Lenguaje. En este caso lo denominamos como Query, el cual se refiere al lenguaje que se utiliza para interactuar con la base de datos, esta nos permite: realizar consultas, insertar datos, actualizar registros y eliminar informacion de la base de datos.
2. Motor. Es lo que permite estructurar toda la base de datos dentro del servidor, es decir es el software responsable de gestionar y manipular los datos almacenados en la base de datos.
3. Servidor. es basicamente un equipo que tiene un procesador y RAM donde se ejecuta el motor de la base de datos, la cual puede ser fisica o virtual que aloja y ejecuta el software de gestion de base de datos.

PostgreSQL se caracteriza:

* Open Source. Codigo abierto, quiere decir que permite a los desarrolladores que interactuan con esta base de datos, se encuentra en contants actualizacion y mejoras logrando ser una de las bases de datos con mayor interaccion y actualizaciones.
* Objeto-Relacional. Dentro del desarrollo de PostgreSQL este utiliza dentro de su nucleo el Objeto-Relacional lo que permite que las bases de datos mantengan una estructura y tuvieran un Desarrollo Orientada a Objetos, en donde se cuenta con herencias, interfaces, lo cual permite que las tablas se puedan relacionar entorno a un concepto y estas tuvieran un direccionamiento congruente.

Estos dos modulos adicionales a PostgreSQL en donde permiten el desarrollo de codigo dentro de la base de datos, en ellas encontramos a:

* PostGIS. Permite convertir el sistema de base de datos PostgreSQL en una base de datos de geolocalización el cual pemrite multiples funciones relacionadas a mapas, puntos geograficos. PL/PgSQL 
* PL/PgSQL. es el lenguaje de programación determinado para PostgreSQl que permite ejecutar comandos en SQL mediante sentencias imperativas y uso de funciones, lo que permite un control automatico que las sentencias basicas de SQL

¿Que es el Estandar ACID en la base de datos?.

El estandar ACID, son una seria de reglas que deben cumplir las bases de datos, las cuales permiten garantizar la integridad y fiabilidad de las operaciones en las bases de datos, lo que resulta en un estandar de calidad y confiabilidad para las operaciones de las bases de datos. 

"ACID" es un acrónimo que representa las siguientes caracteristicas:

* A: Atomicity - Atomicidad: Asegura que una transacción sea ejecutada completamente o no. Es decir que, si una parte de la transaccion falla, la transacción completa se revierte a su estado inicial (rollback), esto deja la base de datos en un estado coherente y no permite transacciones parciales.

* C: Consistency - Consistencia: Esta garantiza que solamente sean aplicados cambios a las bases de datos que la mantengan en un estado valido según las reglas definidas, es decir que todo lo que desarrolle en base al objeto relacional, los datos deben ser congruentes.

* I: Isolation - Aislamiento: Asegura que los efectos de una transacción sean invisibles para otras transacciones y solo sera visible cuando todas se completen. Es decir que cada función que le damos dentro de la base de datos va a trabajar de manera independiente y sin que interfiera con las otras transacciones, permitiendo la coherencia de los datos al finalizar cada una de sus tareas y mostrando el resultado.

* D: Durability: Durabilidad: Asegura que cada vez que realizamos una transaccion con exito, los cambios realizados por esa transacción seran almacenados en una bitacora que cuenta el programa, incluso en casos de falla de sistema, fallo del hardware o reinicio del servidor, los datos que fueron registrados seran recuperados en una ultima transacción realizada.

## ¿Como instalar PostgreSQL?

1. Vamos al navegador, posteriormente escribimos postgreSQL.
2. Enseguida seleccionamos la primera opción que registra y damos clic en ella.
   
![navegador](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/bd22a3ce-5250-49c6-a185-2d0c683a03da)

4.  Al abrir encontraremos la portada el cual damos clic en la opcion Download (descarga).
   
   ![download](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/34f1f2ab-51ba-4867-88e1-6ffbf9514bd2)
   
6.  Al abrir la siguiente pagina, nos pregunta en que sistema operativo deseamos instalar PostgreSQL, en esta opcion damos clic en el sistema operativo que corresponda, en mi caso corresponde a windows.

![sistema operativo](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/363c275b-6768-46b7-92f1-b5ab43667145)

8.  Al dar clic en el sistema operativo windows (en mi caso), nos genera re direcciona a la opcion de descarga, pero antes de descargar vamos a tener en cuenta algunas cosas interesante que veremos aqui.

* En el Banner superior nos indica la ultima version de PostgreSQL esta disponible para el sistema operativo y cual era la version anterior, esto ya que en muchas veces algunas bases de datos que son trabajadas en alguns proyectos son compatibles y no siempre la ultima version cuenta con plugins (conectores) que esten relacionados entre las versiones de las bases de datos.
 
![banner](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/7588961f-b2cb-48ca-bceb-27c5bfc5d29b)

* Posteriormente encontraremos el cuerpo de la pagina, en donde nos da una lectura de lo que incluye esta version pues no es solamente PostgreSQL la unica herramienta que utilizaremos, hay mas conectores que permiten interfaz graficas con el usuario como lo es pgAdmin, pues es la que administra la escritura y ejecuta la consulta en PostgreSQL, entre otras herramientas utiles al respecto.
 
![cuerpo](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/7bb88626-4c87-444a-8e7a-421b17305c7c)

* Enseguida encontraremos a que plataforma de Windows (en este caso) es la version de PosgreSQl mas adaptada para trabajar, pues esta debe soportar la plataforma que se encuentra windows (32 Bits o 64 Bits), esto nos permitira tener una experiencia de trabajo mas optimo en nuestro sistema sin tener riesgos que afecte el rendimiento de nuestra primera herramienta de trabajo.
 
![soporte](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/0f893136-0ef6-4479-9492-013f7daf88f8)

* En el footer (pie de pagina) encontraremos el git de PostgreSQL, en la cual podremos encontrar el repositorio de todos los errores que los usuarios han reportado y que pemrite alimentar para mejorar la siguiente version de PostgreSQL.
 
![github](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/019231a5-cdbf-4f5e-bd43-29b2bf753347)

Lo podra encontrar en el siguiente enlace [git.postgresql.org](https://git.postgresql.org/gitweb/?p=postgresql.git)

![repositorio](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/dbfc58ff-ba80-43c9-ac47-102f04471986)

"Ahora continuaremos con neustra descarga."

9.  Al dar clic en donde dice [Descargue el instalador](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) nos re direcciona a la siguiente pagina, este realizxa un test rapido, el cual nos indica que tipo de version de PostgreSQL al Sistema Operativo soporta y procedemos a descargar. En mi caso soporta la ultima version de PostgreSQL en el sistema Windows x86 - 64

![descarga postgreSQL](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/861ec4dc-1096-423e-96ce-75977c0d41bb)

10.  Al ir a nuestra carpeta de Descargas en nuestro PC, damos clic a la descarga que acabamos de realizar.

![descarga equipo](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/14d01e31-6334-4ce0-a7c5-479aba8b12ba)

11. Este nos abre una ventana la cual es el instalador de PostgreSQL, dando clic en siguiente seguimos las instrucciones respectivas.

![instalador](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/c4f37e14-08df-41fa-9eb9-ceae506eeada)

En mi caso, como previamente tengo instalado el programa, solo me va a dar la opcion de actualizar en caso de que exista alguna actualizacion de version o de plugin.

12.  Al finalizar la descarga daremos clic en Terminar y ya tenemos instalado el programa PostgreSQL en nuestro equipo para comenzar a trabajar en el.

![terminar](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/983f8be8-cc1c-4e34-b418-ee4a948ddb18)


<br>

## ¿Que es pgAdmin?

Es la plataforma de administración y desarrollo de condigo abierto  o tambien conocida como la Interfaz Grafica, esta disponible en los diferentes programas como lo son Linux, Unix, Mac OS X y Windows.

## ¿Como ejecutar y conectarnos a la Interfaz Grafica "pgAdmin"?

1. Ahora en nuestro escritorio buscamos pgadmin y este le damos clic en abrir.

![pgadmin4](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/7a726b54-6e5a-480f-93e0-b305c522316a)

2. Al abrir nos encontraremos con el entorno de pgAdmin4 y asi poder hacer uso de esta base de datos.

![entorno_pgadmin4](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/56d9809f-acd1-4a12-8229-a568d7c91e55)

3. En la parte izquierda se va a encontrar todas las conexiones a los servicios de bases de datos, es decir que podras ver todas las bases de datos que estas conectado, en ella se podran alistar, crear y ver las tablas.
   
![pgadminbd](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/9face195-e1dd-4c00-b780-c7c00f0e2d9a)

4. Ahora en la parte superior de pgAdmin, se encontrara toda la configuración respectiva Archivos, Objeto. Herramientas y Ayuda.

![pgAdmin_banner](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/8dba943e-a9dc-40e1-aadf-976e28f3d9a4)


5. En la parte derecha encontraremos las propiedades, el rendimiento de la base de datos, las conexiones y tableros para visualizar en la interfaz.

![pgadmin_propiedades](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/b65ae182-c357-4dd9-aff4-935273a5e04a)
   
## ¿Como conectarnos a una Base de Datos?

1. 
