# Ejercicios — Tema 5
# Modelo E/R extendido. Restricciones

---

## Ejercicio 1 — Restricciones de inclusión y exclusión

Indica el tipo de restricción que se presenta en cada ejemplo (inclusión o exclusión) y representa gráficamente su diagrama correspondiente:

1. Un estudiante puede asistir a una clase presencial o participar en una clase online, pero no estar en ambas clases al mismo tiempo.

2. El profesor Luis puede impartir el curso "Bases de Datos" o recibir el curso "Inteligencia Artificial", pero no puede impartir y recibir "Bases de Datos" al mismo tiempo.

3. Supongamos que un profesor puede dar e impartir cursos, pero no puede hacer las dos cosas simultáneamente. Existirán por tanto dos relaciones, `IMPARTE` y `RECIBE`, entre las entidades `PROFESOR` y `CURSO`.

4. Un profesor puede impartir un curso en concreto si previamente lo ha recibido.

5. Imaginemos que, para que un `PROFESOR` de Formación Profesional pueda `IMPARTIR` la asignatura de Bases de Datos, debe haber cursado (en este caso, "recibido") anteriormente una ingeniería informática o de telecomunicaciones.

