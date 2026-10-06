# Ejercicios — Tema 4
# El Modelo de Datos. Fases y Modelo E/R

---

## Ejercicio 1 — Cardinalidad en distintos contextos

Para cada una de las siguientes situaciones, indica qué tipo de cardinalidad (1:1, 1:N o M:N) tiene la relación descrita:

1. Un DNI identifica a una única persona, y una persona tiene un único DNI.
2. Un profesor imparte varias asignaturas, pero cada asignatura la imparte un solo profesor.
3. Un alumno se matricula en varios cursos, y un curso tiene varios alumnos matriculados.
4. Un departamento tiene varios empleados, pero cada empleado pertenece a un único departamento.
5. Un país tiene una única capital, y una ciudad es capital de un único país.

---

### Ejercicio 2 — Academia de cursos

A partir del siguiente enunciado, identifica entidades, atributos y relaciones:

> Una academia quiere gestionar sus cursos. Cada curso tiene un código, un nombre y una duración en horas. Cada curso lo imparte un único profesor, aunque un profesor puede impartir varios cursos. Los alumnos se matriculan en los cursos: un alumno puede matricularse en varios cursos, y un curso puede tener varios alumnos matriculados. De cada alumno se guarda el DNI, nombre y teléfono. De cada profesor se guarda el DNI, nombre y especialidad.


---


### Ejercicio 3 — Empresa, clientes, productos y proveedores

A partir del siguiente enunciado se desea realizar el modelo entidad-relación:

> Una empresa vende productos a varios clientes. Se necesita conocer los datos personales de los clientes (nombre, apellidos, DNI, dirección y fecha de nacimiento). Cada producto tiene un nombre y un código, así como un precio unitario. Un cliente puede comprar varios productos a la empresa, y un mismo producto puede ser comprado por varios clientes. Puede haber clientes dados de alta sin comprar productos. Se necesita registrar la fecha de compra de los productos por cada cliente. Los productos son suministrados por diferentes proveedores. Se debe tener en cuenta que un producto solo puede ser suministrado por un proveedor, y que un proveedor puede suministrar diferentes productos. De cada proveedor se desea conocer el NIF, nombre y dirección.

---

### Ejercicio 4 — Empresa de transportes

A partir del siguiente enunciado se desea realizar el modelo entidad-relación.

> Se desea informatizar la gestión de una empresa de transportes que reparte paquetes por toda España. Los encargados de llevar los paquetes son los camioneros, de los que se quiere guardar el dni, nombre, teléfono, dirección, salario y población en la que vive. De los paquetes transportados interesa conocer el código de paquete, descripción, destinatario y dirección del destinatario. Un camionero distribuye muchos paquetes, y un paquete sólo puede ser distribuido por un camionero. De las provincias a las que llegan los paquetes interesa guardar el código de provincia y el nombre. Un paquete sólo puede llegar a una provincia. Sin embargo, a una provincia pueden llegar varios paquetes. De los camiones que llevan los camioneros, interesa conocer la matrícula, modelo, tipo y potencia. Un camionero puede conducir diferentes camiones en fechas diferentes, y un camión puede ser conducido por varios camioneros.

---

### Ejercicio 5 — Empresa de automóviles

> Se desea diseñar una base de datos para almacenar y gestionar la información empleada por una empresa dedicada a la venta de automóviles, teniendo en cuenta los siguientes aspectos:
>
> - La empresa dispone de una serie de coches para su venta. Se necesita conocer la matrícula, marca y modelo, el color y el precio de venta de cada coche.
>
> - Los datos que interesa conocer de cada cliente son el NIF, nombre, dirección, ciudad y número de teléfono: además, los clientes se diferencian por un código interno de la empresa que se incrementa automáticamente cuando un cliente se da de alta en ella. Un cliente puede comprar tantos coches como desee a la empresa. Un coche determinado solo puede ser comprado por un único cliente.
>
> - El concesionario también se encarga de llevar a cabo las revisiones que se realizan a cada coche. Cada revisión tiene asociado un código que se incrementa automáticamente por cada revisión que se haga. De cada revisión se desea saber si se ha hecho cambio de filtro, si se ha hecho cambio de aceite, si se ha hecho cambio de frenos u otros. Los coches pueden pasar varias revisiones en el concesionario.


---

### Ejercicio 6 — Clasifica el tipo de atributo

Para cada atributo, indica de qué tipo es (identificador, descriptivo, derivado, multivaluado o compuesto):

1. El DNI de un cliente.
2. La edad de un empleado, calculada a partir de su fecha de nacimiento.
3. Los distintos números de teléfono de un proveedor (fijo y móvil).
4. La dirección de un cliente (calle, número, ciudad).
5. El nombre de un producto.
6. El e-mail de un cliente puede ser un dato que tengan o quizás no tengan e-mail.


---

### Ejercicio 7 — Mentor (tiene reflexiva)

> A continuación se expondrán los requisitos que se van a considerar en este apartado para llevar a cabo el diseño de la base de datos. 
>
> - La información que se desea almacenar en la Base de Datos se refiere a los alumnos matriculados en cada curso, teniendo en cuenta la fecha de inicio y fecha de finalización de cada alumno en un determinado curso y sabiendo que un alumno se ha podido matricular de uno o varios cursos y que un curso tiene como mínimo a un alumno.
> - De los alumnos se desea saber el nombre completo, dirección, teléfono, nacionalidad y la dirección de correo electrónico. La dirección de correo electrónico es imprescindible para poder realizar los cursos y además es única para cada alumno. 
> - La información referente a los cursos consta del nombre, título del libro de consulta (hay cursos que no utilizan ningún libro de referencia) y url de internet donde se encuentra todo el material que se puede utilizar durante el curso.
> - Cada curso tiene asociado un tutor, la información que se quiere almacenar en la BD acerca de los tutores es la siguiente: DNI, nombre completo, dirección de correo electrónico (puede tener varias). No hay que olvidar que un tutor tutoriza varios cursos y que además un curso puede tener más de un tutor (como pasa en 1er de DAM)
> - **(Reflexiva)**: Un tutor coordina a varios tutores(como mínimo a uno) y un tutor es coordinado por otro tutor.
> - El proyecto MENTOR, además tiene en cuenta que ha de facilitar a los alumnos el acceso a Internet y por lo tanto ha instalado aulas con todos los servicios necesarios para el pleno desarrollo de los cursos. Cada alumno pertenece únicamente a un aula, pueden haber aulas vacías sin alumnos asignados.
> - El mantenimiento de las aulas se lleva a cabo por los administradores de aula. Cada aula tiene asignado un código único, un nombre y dirección. La información que se necesita de cada administrador es su DNI, nombre completo, dirección de correo electrónico (si tiene). Cada aula es administrada por un único administrador y estos pueden administrar varias aulas o ninguna.

---


### Ejercicio 8 - Instituto

>A partir del siguiente enunciado diseñar el modelo entidad-relación de una base de datos d eun instituto:
>
> - De cada profesor se guarda el DNI, nombre, dirección y teléfono.
> -De cada curso se guarda un código y un nombre (por ejemplo, 1º DAM). Un curso tiene varias asignaturas, y cada asignatura pertenece a un único curso.
> - Los profesores imparten asignaturas. De cada asignatura se guarda un código y un nombre.
> - Un profesor puede impartir varias asignaturas, y puede haber profesores sin ninguna asignatura asignada todavía. Toda asignatura es impartido por un único profesor.
> - De cada alumno se guarda el número de expediente, nombre, apellidos y fecha de nacimiento.
> - Cada alumno está matriculado en una o varias asignaturas, y cada asignatura tiene al menos un alumno matriculado.
> - En cada curso (por ejemplo, 1º DAM) los alumnos eligen un delegado, que es otro alumno. Interesa saber quién es el delegado de cada alumno. Un alumno puede ser delegado de varios compañeros o de ninguno. Cada alumno tiene como mucho un delegado, y los propios delegados no tienen delegado.


---


