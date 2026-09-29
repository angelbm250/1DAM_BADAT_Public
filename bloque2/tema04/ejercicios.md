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

A partir del siguiente enunciado, identifica entidades, atributos y relaciones (todavía sin dibujar el diagrama):

> Una academia quiere gestionar sus cursos. Cada curso tiene un código, un nombre y una duración en horas. Cada curso lo imparte un único profesor, aunque un profesor puede impartir varios cursos. Los alumnos se matriculan en los cursos: un alumno puede matricularse en varios cursos, y un curso puede tener varios alumnos matriculados. De cada alumno se guarda el DNI, nombre y teléfono. De cada profesor se guarda el DNI, nombre y especialidad.


---


### Ejercicio 3 — Empresa, clientes, productos y proveedores

A partir del siguiente enunciado se desea realizar el modelo entidad-relación:

> Una empresa vende productos a varios clientes. Se necesita conocer los datos personales de los clientes (nombre, apellidos, DNI, dirección y fecha de nacimiento). Cada producto tiene un nombre y un código, así como un precio unitario. Un cliente puede comprar varios productos a la empresa, y un mismo producto puede ser comprado por varios clientes. Puede haber clientes dados de alta sin comprar productos. Se necesita registrar la fecha de compra de los productos por cada cliente. Los productos son suministrados por diferentes proveedores. Se debe tener en cuenta que un producto solo puede ser suministrado por un proveedor, y que un proveedor puede suministrar diferentes productos. De cada proveedor se desea conocer el NIF, nombre y dirección.

