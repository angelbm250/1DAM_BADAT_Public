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

---

## Ejercicio 5 — StreamWorld

> La empresa StreamWorld desea diseñar una base de datos para gestionar los usuarios y los contenidos audiovisuales que ofrece en su plataforma en línea.
>
> ### Usuarios
>
>- De cada usuario se desea almacenar un identificador único, su nombre, primer apellido, segundo apellido (opcional), correo electrónico y contraseña.
>- Los usuarios pueden ser únicamente **Free** o **Premium**.
>- Los usuarios Free no disponen de información adicional, mientras que de los usuarios Premium se desea almacenar además su teléfono de contacto y la fecha de renovación de la suscripción.
>
>### Visualizaciones
>
>- Los usuarios pueden visualizar vídeos en la plataforma. Un usuario puede ver varios vídeos, y un vídeo puede ser visto por varios usuarios.
>- De cada visualización se almacenará la fecha y hora en que se realizó la reproducción de cada usuario.
>
>### Vídeos
>
>- En el sistema se almacenan vídeos, de los cuales se guarda un identificador único, título, sinopsis, imagen, duración y un enlace o archivo de vídeo.
>- Los vídeos pueden ser de dos tipos: **Películas** y **Episodios**.
>- De las películas se desea almacenar su puntuación en IMDb y el nombre del director.
>- De los episodios se desea almacenar el número del episodio y la temporada a la que pertenece.
>- Cada episodio está asociado a una única serie, mientras que una serie puede tener varios episodios.
>- De cada serie se desea registrar un identificador único y un nombre.
>
>### Géneros
>
>- Cada vídeo (película o episodio) puede clasificarse en uno o varios géneros (por ejemplo: acción, comedia, drama, ciencia ficción, etc.).
>- De cada género se almacenará un identificador único y un nombre. Un vídeo puede pertenecer a varios géneros y un mismo género puede aplicarse a varios vídeos.


---

## Ejercicio 6 — Instituto: profesores, módulos, alumnos y grupos

> Un instituto desea implementar una base de datos para gestionar la información de sus profesores, módulos, alumnos y grupos. A continuación se describen los requisitos necesarios para el diseño de esta base de datos.
>
>- La base de datos debe almacenar el DNI, nombre, dirección y teléfono de cada profesor.
>- Los profesores pueden **impartir** o **recibir** uno o varios módulos.
>- Cada módulo está asignado exclusivamente para que lo imparta un profesor, y lo pueden recibir varios profesores.
>- Hemos de modelar que, para que un profesor pueda impartir un módulo concreto, previamente lo ha tenido que recibir.
>
>- Cada módulo tiene un código único y un nombre, y tiene alumnos matriculados.
>- Un alumno puede estar matriculado en varios módulos, pero un módulo tiene como mínimo un alumno inscrito.
>
>- De cada alumno se guarda el número de expediente, nombre, apellidos, fecha de nacimiento y edad (que se calculará a través de la fecha de nacimiento).
>- Además, cada alumno tiene un correo electrónico que se utiliza para recibir comunicaciones del instituto.
>- La base de datos debe registrar una relación en la que algunos alumnos actúan como **responsable** de otros alumnos (por ejemplo, en programas de ayuda entre alumnos de distintos niveles).
>- Un alumno puede actuar como responsable de varios alumnos (puede no tener alumnos a cargo), y cada alumno puede tener un único alumno responsable o ninguno.

---

## Ejercicio 7 — Taller de mecánica

> Un taller de mecánica de automóviles desea tener una base de datos para llevar la gestión de las reparaciones de vehículos, de los clientes y empleados del taller, así como de las piezas que se utilizan en las reparaciones que se llevan a cabo en el taller. Los supuestos semánticos que deben recogerse en el esquema E/R se describen a continuación:
>
> ### Empleados
>
> - En el taller existen varios empleados de los que se quiere guardar su DNI, nombre, dirección, teléfono de contacto y fecha de incorporación al taller.
> - Estos empleados pueden ser únicamente de dos tipos: **mecánicos**, de los que se quiere conocer su especialidad (por ejemplo, motores de inyección, carburadores, etc.), y **aprendices**.
> - Un aprendiz es supervisado en su trabajo por un mecánico, y un mecánico puede supervisar a varios aprendices (aunque puede ser que haya mecánicos que no supervisen a ningún aprendiz).
> - Tanto los mecánicos como los aprendices participan en las reparaciones de vehículos que se realizan en el taller.
>
> ### Reparaciones
>
> - Cada reparación se caracteriza por un código de reparación, una fecha de inicio, una fecha de fin (opcional, ya que hay reparaciones en curso), una descripción del trabajo realizado, así como una duración en horas.
> - Una reparación corresponde a un único vehículo, y un vehículo puede haber sufrido varias reparaciones, es decir, un vehículo puede haber pasado por el taller en diversas ocasiones.
> - Interesa recoger las horas que un determinado empleado trabaja en cada reparación que tiene asignada. Un empleado puede trabajar en varias reparaciones, y en una reparación puede haber varios empleados trabajando.
>
> ### Vehículos y clientes
>
> - De los vehículos que entran en el taller se guarda su matrícula, marca, modelo y color, así como la compañía en la que está asegurado junto con su correspondiente número de póliza (no es necesario crear una entidad de compañías de seguros).
> - También se guarda información sobre los clientes (NIF, nombre, dirección y teléfono de contacto).
> - Un vehículo pertenece a un único cliente del taller, y un cliente puede tener varios vehículos.
>
> ### Piezas
>
> - Puede ocurrir que una reparación requiera una o varias piezas para sustituir las dañadas.
> - La base de datos contiene información sobre las piezas (código de pieza, precio por unidad, fabricante y una descripción).
> - Es necesario guardar también el número de unidades que se necesita de una determinada pieza en cada reparación de un vehículo.
> - En una reparación se pueden usar diferentes piezas, y el mismo código de pieza se puede usar en varias reparaciones.