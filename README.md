# Curso Introducción a la Base de Datos con PostgreSQL.
<br>

## Descripción.

Introducción practica a PostgresSQL, al ser un sistema de gestión de Base de Datos relacional, se aprenderá desde 
la instalación y configuración del entorno hasta el modelado de los datos, consultas SQL y administración eficiente 
de Bases de Datos en entornos reales, en donde se tendrán en cuenta aspectos teóricos y prácticos relacionados con 
la seguridad y la integridad de los datos.

<br>

## ¿Que es y para que sirve PostgreSQL?
Es un sistema de gestión de bases de datos relacional de código abierto y de alto rendimiento. Es conocido por su fiabilidad, robustez y capacidad para manejar grandes volúmenes de datos. PostgreSQL es altamente compatible con los estándares SQL y admite una amplia gama de tipos de datos, funciones y características avanzadas, lo que lo hace ideal para aplicaciones empresariales y proyectos en general.

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

9.  Al dar clic en donde dice [Descargue el instalador](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) nos re direcciona a la siguiente pagina, este realizxa un test rapido, el cual nos indica que tipo de version de PostgreSQL al Sistema Operativo soporta y procedemos a descargar. En mi caso soporta la ultima version de PostgreSQL en el sistema Windows x86 - 64

![descarga postgreSQL](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/861ec4dc-1096-423e-96ce-75977c0d41bb)

10.  Al ir a nuestra carpeta de Descargas en nuestro PC, damos clic a la descarga que acabamos de realizar.

![descarga equipo](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/14d01e31-6334-4ce0-a7c5-479aba8b12ba)

11. Este nos abre una ventana la cual es el instalador de PostgreSQL, dando clic en siguiente seguimos las instrucciones respectivas.

![instalador](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/c4f37e14-08df-41fa-9eb9-ceae506eeada)

En mi caso, como previamente tengo instalado el programa, solo me va a dar la opcion de actualizar en caso de que exista alguna actualizacion de version o de plugin.

12.  Al finalizar la descarga daremos clic en Terminar y ya tenemos instalado el programa PostgreSQL en nuestro equipo para comenzar a trabajar en el.

![terminar](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/983f8be8-cc1c-4e34-b418-ee4a948ddb18)

13.  Ahora en nuestro escritorio buscamos pgadmin y este le damos clic en abrir.

![pgadmin4](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/7a726b54-6e5a-480f-93e0-b305c522316a)

14. Al abrir nos encontraremos con el entorno de pgAdmin4 y asi poder uso de esta base de datos.

![entorno_pgadmin4](https://github.com/camilomejiar/Curso-Introducci-n-a-la-Base-de-Datos-con-PostgreSQL./assets/101876440/56d9809f-acd1-4a12-8229-a568d7c91e55)
