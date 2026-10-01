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

