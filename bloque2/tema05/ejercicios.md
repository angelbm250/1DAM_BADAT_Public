# Ejercicios — Tema 5
# Modelo E/R extendido. Restricciones

---

## Ejercicio 1 — Restricciones de inclusión y exclusión

Para cada uno de los siguientes casos, identifica qué tipo de restricción sobre relaciones (exclusividad, inclusividad, inclusión o exclusión) se ajusta mejor:

1. Un estudiante puede asistir a una clase presencial o participar en una clase online, pero no estar en ambas clases al mismo tiempo.

2. El profesor Luis puede impartir el curso "Bases de Datos" o recibir el curso "Inteligencia Artificial", pero no puede impartir y recibir "Bases de Datos" al mismo tiempo.

3. Supongamos que un profesor puede dar e impartir cursos, pero no puede hacer las dos cosas simultáneamente. Existirán por tanto dos relaciones, `IMPARTE` y `RECIBE`, entre las entidades `PROFESOR` y `CURSO`.

4. Un profesor puede impartir un curso en concreto si previamente lo ha recibido.

5. Imaginemos que, para que un `PROFESOR` de Formación Profesional pueda `IMPARTIR` la asignatura de Bases de Datos, debe haber cursado (en este caso, "recibido") anteriormente una ingeniería informática o de telecomunicaciones.

---

## Ejercicio 2 — Empresa y tipos de empleados

> Una empresa gestiona la información de sus empleados y clasifica a los mismos según el tipo de puesto que ocupan. Los empleados tienen un DNI (clave primaria), un nombre y ocupan uno de los siguientes tipos de puestos: Directivo, Técnico o Comercial.
>
> - Los **Directivos** pertenecen a un departamento, identificado por el campo `Dpto`.
> - Los **Comerciales** reciben un porcentaje de comisión, identificado por el campo `%Comisión`.
> - Los **Técnicos** manipulan máquinas en su labor. Cada máquina está identificada por un número de serie (`nº serie`) y tiene una descripción (`descripción`). Un Técnico puede manipular varias máquinas, pero cada máquina solo puede ser manipulada por un técnico asignado.


---

## Ejercicio 3 — Técnicos y proyectos

> Modelo entidad-relación extendido para un sistema de gestión de técnicos y su asignación a proyectos dentro de una empresa u organización.
>
> - Existen los **empleados**, que pueden ser solo administrativos o técnicos; únicamente podrán cumplir una de las funciones en la empresa. De todos los empleados interesa saber el DNI, nombre y dirección.
> - Un **departamento** tiene uno o varios empleados, y un empleado puede trabajar simultáneamente en un único departamento. De los departamentos interesa guardar su código y el nombre.
> - Los **técnicos** trabajan con proyectos, ya que no todos los empleados de la empresa, como los administrativos, son susceptibles de trabajar en un proyecto. De los técnicos interesa saber también el atributo nivel. Un técnico puede trabajar en uno o varios proyectos, y en un proyecto trabajan uno o varios técnicos.
> - De los **proyectos** interesa saber código, nombre, fecha de inicio y fecha final. Los proyectos se asignan a un cliente, pero hay clientes que pueden estar en varios proyectos de seguimiento. De los **clientes** interesa saber el NIF, nombre y dirección.
> - Por otro lado, interesa saber la fecha de asignación y la fecha de cese, ya que un técnico no siempre estará trabajando en un proyecto, sino en un determinado periodo.

---

## Ejercicio 4 — Instituto: profesores, asignaturas y coordinadores

> Un instituto académico requiere organizar la información de los profesores, asignaturas y coordinadores en un sistema de base de datos. 
>
> - **Profesores:** cada profesor tiene un DNI que lo identifica de manera única, además de información adicional como su categoría y la fecha de ingreso al instituto.
> - **Asignaturas:** cada asignatura tiene un código único, una descripción y un valor en créditos. Algunas asignaturas tienen créditos adicionales denominados `creditosp`.
> - **Coordinadores:** son responsables de coordinar asignaturas. Cada coordinador está identificado por su DNI, y además se almacena su nombre, el departamento (`dpto`) al que pertenece y las asignaturas (`asig`) que coordina.
> - Un profesor **prepara** una o más asignaturas, pero puede preparar más de una asignatura. Una asignatura puede ser preparada por más de un profesor.
> - Un profesor **imparte** asignaturas. Un profesor puede impartir una o más asignaturas, y una asignatura puede ser impartida por varios profesores. Sin embargo, un profesor solo puede impartir una asignatura si previamente la ha preparado. 
> - Los coordinadores **coordinan** las asignaturas. Un coordinador puede estar encargado de coordinar una o más asignaturas, y una asignatura puede ser coordinada por más de un coordinador.