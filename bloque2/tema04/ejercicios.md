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

> A partir del siguiente enunciado diseñar el modelo entidad-relación de una base de datos de un instituto:
>
> - De cada profesor se guarda el DNI, nombre, dirección y teléfono.
> - De cada curso se guarda un código y un nombre (por ejemplo, 1º DAM). Un curso tiene varias asignaturas, y cada asignatura pertenece a un único curso.
> - Los profesores imparten asignaturas. De cada asignatura se guarda un código y un nombre.
> - Un profesor puede impartir varias asignaturas, y puede haber profesores sin ninguna asignatura asignada todavía. Toda asignatura es impartido por un único profesor.
> - De cada alumno se guarda el número de expediente, nombre, apellidos y fecha de nacimiento.
> - Cada alumno está matriculado en una o varias asignaturas, y cada asignatura tiene al menos un alumno matriculado.
> - En cada curso (por ejemplo, 1º DAM) los alumnos eligen un delegado, que es otro alumno. Interesa saber quién es el delegado de cada alumno. Un alumno puede ser delegado de varios compañeros o de ninguno. Cada alumno tiene como mucho un delegado, y los propios delegados no tienen delegado.

---

### Ejercicio 9 - Feria del libro

> Realiza el esquema Entidad / Interrelación de acuerdo a las siguientes características:
>
> - Se necesita almacenar la información de cada caseta participante en la feria del libro. 
> - Una caseta se identifica por un número y representa a una editorial o librería. Además se almacenará también los metros cuadrados.
> - Las casetas exponen libros y un libro puede estar expuesto en varias casetas.Toda caseta expone al menos un libro y todo libro está expuesto en alguna caseta
> - De cada libro se necesita saber su ISBN (único), título y año de publicación. También es interesante conocer de cada libro el número de ejemplares de los que dispone cada caseta y el precio de venta.
> - También es útil saber los datos de los escritores. De los escritores se almacenará un nombre completo único, un seudónimo si lo tuviera, su fecha de nacimiento y lugar donde nació.
> - Un libro puede no ser escrito por nadie o está escrito por un solo escritor, y un escritor puede escribir más de un libro.
> - Las casetas contratarán a los escritores más importantes del momento (para la firma de sus libros a los visitantes), teniendo en cuenta que una caseta puede contratar a varios escritores. Interesará conocer la fecha y hora en la que los escritores han sido contratados por las casetas para la firma de sus libros

---

### Ejercicio 10 - Pruebas del módulo de Bases de Datos

> - Los profesores del módulo de Bases de Datos deciden crear una base de datos que contenga la información de los resultados de las pruebas realizadas por los alumnos.
>
> - De los alumnos se guarda un identificador único, NIF, nombre, apellidos, fecha de nacimiento y el grupo al que asisten a clase. Se guarda también un teléfono de contacto, opcional (hay alumnos que no lo han facilitado). Interesa además conocer la edad de cada alumno, que se calcula a partir de su fecha de nacimiento.
> - Los alumnos realizan dos tipos de pruebas a lo largo del curso:
> - **Exámenes teóricos**. Se definen por un identificador único, un título, el número de preguntas y la fecha de realización, que es la misma para todos los alumnos que hacen el mismo examen. Cada alumno realiza varios exámenes (al menos uno) y hay que guardar la nota de cada alumno en cada examen. Puede haber exámenes creados que todavía no ha realizado ningún alumno.
> - **Prácticas**. Se realiza un número indeterminado de prácticas durante el curso. Se definen por un identificador, un título y el grado de dificultad (Baja, Media o Alta). Los alumnos pueden examinarse de cualquier práctica cuando lo deseen, como mucho una vez cada una, y se guarda la fecha y la nota obtenida. Un alumno puede no haber hecho ninguna práctica, y puede haber prácticas que nadie ha hecho aún.
> - De los profesores se guarda un identificador, NIF, nombre y apellidos. Interesa saber qué profesor o profesores han participado en el diseño de una práctica. En el diseño de una práctica colabora al menos un profesor, y puede colaborar más de uno. Un profesor puede diseñar varias prácticas, o ninguna.Se guarda la fecha en que cada profesor participó en el diseño de la práctica. Si participa en fechas distintas.

**Entrega**: realizar el diagrama entidad-relación con Dia y subirlo al repositorio Git de la asignatura. Hay que subir el fichero .dia y también una exportación en .png, en el que aparezca vuestro nombre.

---

### Ejercicio 11 - Centro de salud (versión binaria)

> Un centro de salud quiere gestionar la información de sus médicos, pacientes y medicamentos.
>
> - De cada **médico** se guarda el número de colegiado, nombre y especialidad.
> - De cada **paciente** se guarda el DNI, nombre y fecha de nacimiento.
> - De cada **medicamento** se guarda un código y un nombre.
> - Cada paciente tiene asignado **un único médico de cabecera**, y es obligatorio que lo tenga. Un médico puede ser el médico de cabecera de muchos pacientes, o de ninguno todavía.
> - Un médico receta habitualmente varios medicamentos, o ninguno todavía. Un mismo medicamento puede ser recetado habitualmente por varios médicos, o por ninguno.
> - Interesa saber qué **medicamentos toma actualmente** cada paciente (varios o ninguno) y qué pacientes toman cada medicamento.
> 
> **Pregunta**: Con los datos de este modelo, ¿podrías saber quién le recetó por ejemplo el ibuprofeno a Ana?. **No**. El modelo sabe que Ana toma ibuprofeno y que el Dr. Ruiz suele recetarlo, pero no que se lo recetó él. Cada relación se lee sola; ninguna une a las tres entidades.

---

### Ejercicio 12 - Centro de salud (versión ternaria)

> Es el mismo centro de salud del ejercicio anterior, con las mismas entidades (médico, paciente y medicamento) y los mismos datos de cada una. Se mantiene el **médico de cabecera** (un único médico por paciente, obligatorio).
>
> Ahora, en lugar las recetas habituales de los médicos y de los medicamentos que toma cada paciente, el centro necesita registrar **las recetas**:
>
> - Cada receta indica **qué médico receta qué medicamento a qué paciente**, y la **fecha** en que se emite.
> - Para un paciente y un medicamento concretos solo hay **un único médico** que lo receta. 
> - Un médico puede recetar el mismo medicamento a muchos pacientes
> - Un médico puede recetar a un mismo paciente varios medicamentos distintos.
> - Puede haber médicos que aún no han recetado nada, pacientes sin recetas y medicamentos que nunca se han recetado.
>
> Por ejemplo, hoy el centro tiene estas recetas:
>
> | Médico | Medicamento | Paciente | Fecha |
> |---|---|---|---|
> | Dra. López | Ibuprofeno | Ana | 03/10 |
> | Dr. Ruiz | Paracetamol | Ana | 05/10 |
> | Dr. Ruiz | Ibuprofeno | Luis | 05/10 |

> | Par | Qué fijas | Qué cuentas | Ejemplo con los datos | Resultado |
> |---|---|---|---|---|
> | **(0,1)** junto a `MÉDICO` | un paciente y un medicamento: *Ana + ibuprofeno* | cuántos médicos | solo López. No puede haber dos. Y > si Ana nunca ha recibido ibuprofeno, ninguno | de 0 a **1** |
> | **(0,N)** junto a `PACIENTE` | un médico y un medicamento: *Ruiz + ibuprofeno* | cuántos pacientes | Luis, y podrían ser más | de 0 > a **N** |
> | **(0,N)** junto a `MEDICAMENTO` | un médico y un paciente: *Ruiz + Ana* | cuántos medicamentos | paracetamol, y podría haber más | 
> de 0 a **N** |


---

### 13 - Hoteles y habitaciones

> Una cadena hotelera quiere guardar información de sus hoteles y habitaciones.
>
> - De cada hotel se guarda un código (único), nombre, ciudad y categoría (número de estrellas).
> - De cada habitación se guarda el número de habitación, la planta y el tipo (individual, doble o suite).
> - Los números de habitación se repiten entre hoteles: por ejemplo, todos los hoteles tienen una habitación 101. Dentro de un mismo hotel, el número es único.
> - Toda habitación pertenece a un único hotel y no tiene sentido sin él: si se elimina un hotel, desaparecen sus habitaciones ovbiamente. Todo hotel tiene al menos una habitación.
> - De cada cliente se guarda el DNI, nombre y teléfono. Un cliente se aloja en una o varias habitaciones (solo se registran clientes que se han alojado alguna vez), y en una habitación se pueden haber alojado varios clientes, o ninguno todavía. De cada estancia se guarda la fecha de entrada y la fecha de salida. Si un cliente se aloja varias veces en la misma habitación, solo se guarda la última estancia.
> - De cada empleado de limpieza se guarda el DNI, nombre y turno (mañana o tarde). Cada habitación tiene asignado un único empleado de limpieza, y cada empleado tiene asignada al menos una habitación. Solo hace falta saber quien tiene asignada ahor ala habitación.