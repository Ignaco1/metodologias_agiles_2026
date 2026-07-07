## Enunciado

### Generar un plan de trabajo basado en SCRUM para resolver la siguiente tarea

**Objetivo:** El objetivo de este ejercicio es que los alumnos universitarios practiquen la creación de historias de usuarios para un sistema informático de presupuesto de construcción de galpones, utilizando la metodología ágil.

### Descripción del ejercicio

1. Los alumnos deberán formar equipos de trabajo, de preferencia de 3 a 5 personas por equipo.

2. Cada equipo deberá seleccionar la temática de construcción de galpones para su sistema informático de presupuesto.

3. Los equipos deberán generar al menos tres historias de usuario para su sistema, basadas en la temática seleccionada. Cada historia de usuario debe incluir un título y una descripción que contenga los criterios de aceptación.

4. Las historias de usuario deben estar enfocadas en las funcionalidades y características del sistema informático, considerando aspectos como la creación de presupuestos detallados, seguimiento del presupuesto durante la construcción, inclusión de etapas, generación de informes, entre otros.

5. Los equipos deben asegurarse de que las historias de usuario sean claras, concisas y comprensibles, siguiendo las buenas prácticas de redacción de historias ágiles.

6. Al finalizar, cada equipo deberá presentar sus historias de usuario al resto de la clase, explicando el contexto de su sistema y los criterios de aceptación de cada historia.

7. Se fomenta el intercambio de ideas y la retroalimentación constructiva entre los equipos durante las presentaciones.

> **Nota:** Los equipos pueden utilizar ejemplos y situaciones hipotéticas para desarrollar las historias de usuario, considerando las necesidades y requisitos típicos de un sistema de presupuesto de construcción de galpones. Además, se recomienda utilizar herramientas como tarjetas o post-its para escribir y visualizar las historias de usuario durante el ejercicio.

---

# Resolución

## 1. Contexto del sistema

Se propone desarrollar **PresuGalpón**, un sistema web para gestionar presupuestos de construcción de galpones metálicos industriales.

El sistema estará destinado a empresas constructoras que necesitan elaborar presupuestos claros, organizar las etapas de cada obra, registrar gastos reales durante la ejecución y generar informes para sus clientes o responsables de proyecto.

El producto buscará resolver problemas habituales del dominio, tales como:

- Demoras al elaborar presupuestos manuales.
- Falta de detalle sobre materiales, mano de obra y equipos.
- Dificultad para conocer cuánto se presupuestó y cuánto se gastó realmente.
- Falta de control sobre las etapas de construcción.
- Necesidad de generar informes comprensibles para clientes y responsables de obra.

---

## 2. Objetivo del producto

El objetivo de **PresuGalpón** es permitir que una empresa constructora cree, controle y consulte presupuestos de galpones de forma organizada.

La primera versión del producto deberá permitir:

- Crear presupuestos detallados.
- Registrar las etapas principales de una obra.
- Asociar costos de materiales, mano de obra y equipos.
- Realizar seguimiento del presupuesto durante la construcción.
- Detectar desvíos entre el presupuesto planificado y el gasto real.
- Generar informes básicos del estado de cada obra.

---

## 3. Equipo Scrum propuesto

Para este ejercicio se propone un equipo de cinco integrantes.

| Rol | Responsabilidad dentro del proyecto |
|---|---|
| Product Owner | Representa las necesidades de la empresa constructora y de los clientes. Define, prioriza y aclara las historias del Product Backlog. También verifica que los criterios de aceptación se cumplan. |
| Scrum Master | Facilita los eventos de Scrum, ayuda al equipo a trabajar de forma organizada, elimina impedimentos y promueve la mejora continua. |
| Equipo de Desarrollo – Integrante 1 | Colabora en el diseño de la interfaz, formularios de presupuesto y visualización de información. |
| Equipo de Desarrollo – Integrante 2 | Colabora en la lógica de negocio, cálculos de costos, validaciones y almacenamiento de datos. |
| Equipo de Desarrollo – Integrante 3 | Colabora en pruebas, control de calidad, elaboración de reportes y validación de criterios de aceptación. |

Aunque cada integrante puede tener mayor participación en determinadas tareas, el Equipo de Desarrollo trabaja de forma conjunta, comparte la responsabilidad sobre el incremento y evita formar subequipos aislados.

---

## 4. Product Goal

> Desarrollar una primera versión funcional de PresuGalpón que permita crear presupuestos de galpones por etapas, registrar gastos reales durante la obra y generar un informe básico para controlar desvíos económicos.

---

## 5. Product Backlog inicial

| ID | Historia de usuario | Prioridad | Estimación | Sprint propuesto |
|---|---|---:|---:|---|
| HU-01 | Crear presupuesto detallado | Muy alta | 8 puntos | Sprint 1 |
| HU-02 | Definir etapas de construcción | Alta | 5 puntos | Sprint 1 |
| HU-03 | Registrar avance y gastos reales | Alta | 8 puntos | Sprint 2 |
| HU-04 | Generar informe de presupuesto | Media | 5 puntos | Sprint 2 |

La estimación se realizará mediante **Planning Poker**, utilizando puntos de historia basados en complejidad, esfuerzo e incertidumbre. El Product Owner explica y aclara cada historia, pero la estimación es responsabilidad del Equipo de Desarrollo.

---

# 6. Historias de usuario

## HU-01 – Crear presupuesto detallado

### Título

**Crear un presupuesto detallado para un galpón**

### Historia de usuario

> Como **presupuestista de una empresa constructora**, quiero **crear un presupuesto detallado de un galpón indicando sus características, materiales, mano de obra y equipos necesarios**, para **conocer el costo estimado de la obra y presentar una propuesta clara al cliente**.

### Descripción

El sistema debe permitir registrar los datos principales del proyecto, como cliente, nombre de la obra, ubicación, tipo de galpón, superficie estimada y fecha de elaboración.

Además, debe permitir incorporar conceptos de presupuesto vinculados con materiales, mano de obra y equipos. Cada concepto deberá incluir una descripción, cantidad, costo unitario y subtotal.

### Criterios de aceptación

- El sistema debe permitir ingresar los datos básicos del proyecto: cliente, nombre de obra, tipo de galpón y superficie estimada.
- El sistema debe permitir agregar ítems de materiales, mano de obra y equipos.
- Cada ítem debe incluir descripción, cantidad, costo unitario y subtotal calculado automáticamente.
- El total del presupuesto debe ser igual a la suma de los subtotales de todos los ítems cargados.
- No se debe permitir guardar un presupuesto sin cliente, obra o al menos un ítem presupuestado.
- No se deben permitir cantidades ni costos unitarios negativos o iguales a cero.
- Al guardar el presupuesto, el sistema debe asignarle un estado inicial de **Borrador**.

### Estimación

**8 puntos de historia**

---

## HU-02 – Definir etapas de construcción

### Título

**Organizar el presupuesto por etapas de obra**

### Historia de usuario

> Como **jefe de obra**, quiero **dividir la construcción del galpón en etapas y asociar costos a cada una**, para **planificar el proyecto y conocer cuánto se prevé invertir en cada fase de la construcción**.

### Descripción

El sistema debe permitir organizar un presupuesto en etapas de obra. Para un galpón se contemplarán inicialmente las siguientes etapas:

1. Preparación del terreno.
2. Fundaciones.
3. Estructura metálica.
4. Cubierta y cerramientos.
5. Instalaciones complementarias.
6. Terminaciones.

Cada ítem del presupuesto deberá estar asociado a una etapa, permitiendo visualizar subtotales por fase.

### Criterios de aceptación

- El sistema debe permitir crear, editar y ordenar etapas de construcción.
- El sistema debe permitir asociar cada ítem presupuestado a una única etapa.
- El sistema debe mostrar el subtotal de cada etapa.
- El sistema debe mostrar el total general del presupuesto.
- La suma de los subtotales por etapa debe coincidir con el total del presupuesto.
- No se debe permitir eliminar una etapa si posee ítems asociados sin antes reasignarlos o eliminarlos.
- El sistema debe permitir utilizar las etapas estándar propuestas o crear una etapa adicional cuando la obra lo requiera.

### Estimación

**5 puntos de historia**

---

## HU-03 – Registrar avance y gastos reales

### Título

**Realizar seguimiento del presupuesto durante la obra**

### Historia de usuario

> Como **supervisor de obra**, quiero **registrar el avance físico de cada etapa y los gastos reales realizados**, para **comparar el presupuesto planificado con el costo ejecutado y detectar desvíos a tiempo**.

### Descripción

Durante la construcción del galpón, el responsable de obra debe poder indicar el porcentaje de avance de cada etapa y registrar los gastos reales efectuados.

El sistema deberá comparar el gasto ejecutado con el monto presupuestado y mostrar desvíos cuando el costo real supere lo estimado.

### Criterios de aceptación

- El sistema debe permitir registrar un porcentaje de avance entre 0% y 100% para cada etapa.
- El sistema debe permitir registrar gastos reales asociados a una etapa.
- Cada gasto debe incluir fecha, descripción, importe y responsable que lo registró.
- El sistema debe mostrar para cada etapa el monto presupuestado, el monto ejecutado y la diferencia.
- Cuando el gasto real de una etapa supere en más de un 10% el presupuesto asignado, el sistema debe generar una alerta.
- El sistema debe conservar un historial de los gastos registrados.
- No se deben permitir gastos negativos ni avances superiores al 100%.

### Estimación

**8 puntos de historia**

---

## HU-04 – Generar informe del presupuesto

### Título

**Generar un informe de presupuesto y avance de obra**

### Historia de usuario

> Como **dueño de la empresa constructora**, quiero **generar un informe del presupuesto y del avance de cada galpón**, para **analizar desvíos, comunicar el estado de la obra al cliente y tomar decisiones económicas**.

### Descripción

El sistema deberá generar un informe por proyecto que reúna los datos principales de la obra, las etapas, los costos presupuestados, los gastos reales, el porcentaje de avance y los desvíos detectados.

### Criterios de aceptación

- El sistema debe permitir seleccionar un proyecto o presupuesto para generar el informe.
- El informe debe incluir los datos principales de la obra y del cliente.
- El informe debe mostrar cada etapa con su presupuesto, gasto ejecutado, diferencia y porcentaje de avance.
- El informe debe resaltar las etapas que presenten desvíos superiores al límite establecido.
- El informe debe mostrar el total presupuestado, el total ejecutado y la diferencia general.
- El usuario debe poder visualizar el informe antes de descargarlo o imprimirlo.
- El sistema debe registrar la fecha de generación del informe.

### Estimación

**5 puntos de historia**

---

## 7. Validación de las historias de usuario

Las historias propuestas siguen las buenas prácticas de redacción ágil:

| Característica | Aplicación en las historias |
|---|---|
| Independientes | Cada historia representa una necesidad concreta y puede planificarse de forma separada. |
| Negociables | Los detalles de interfaz, formato de informe y etapas pueden refinarse junto con el Product Owner. |
| Valiosas | Todas aportan valor para la empresa constructora, el jefe de obra o el cliente. |
| Estimables | Se pueden estimar mediante Planning Poker porque poseen alcance y criterios claros. |
| Pequeñas | Se dividen en funcionalidades abordables dentro de uno o dos Sprints. |
| Testeables | Cada historia cuenta con criterios de aceptación verificables. |

---

# 8. Plan de trabajo basado en Scrum

## 8.1 Preparación inicial

Antes del primer Sprint se realizará una instancia de preparación inicial para:

- Definir la visión del producto.
- Acordar el Product Goal.
- Identificar usuarios, stakeholders y necesidades principales.
- Crear y ordenar el Product Backlog inicial.
- Definir los roles Scrum.
- Establecer criterios de Definition of Ready y Definition of Done.
- Preparar un tablero visual con tarjetas o post-its.

---

## 8.2 Duración de los Sprints

Se propone trabajar con **Sprints de dos semanas**.

Esta duración permite desarrollar incrementos pequeños, recibir feedback frecuente y ajustar las historias antes de continuar con funcionalidades más complejas.

---

## 8.3 Sprint 1 – Presupuesto inicial por etapas

### Sprint Goal

> Permitir que la empresa cree un presupuesto inicial de un galpón, organizado por etapas de construcción.

### Historias seleccionadas

- HU-01 – Crear presupuesto detallado.
- HU-02 – Definir etapas de construcción.

### Sprint Backlog

| Historia | Tareas principales |
|---|---|
| HU-01 | Diseñar formulario de presupuesto, crear validaciones, registrar ítems, calcular subtotales y total general. |
| HU-02 | Definir catálogo inicial de etapas, asociar ítems a etapas, calcular subtotales por etapa y mostrar el resumen. |

### Incremento esperado

Al finalizar el Sprint 1, el usuario podrá:

- Crear un presupuesto de galpón.
- Cargar materiales, mano de obra y equipos.
- Asociar los ítems a una etapa.
- Visualizar subtotales por etapa.
- Consultar el total estimado de la obra.

---

## 8.4 Sprint 2 – Seguimiento e informes

### Sprint Goal

> Permitir controlar el gasto real y el avance de una obra, generando información útil para la toma de decisiones.

### Historias seleccionadas

- HU-03 – Registrar avance y gastos reales.
- HU-04 – Generar informe de presupuesto.

### Sprint Backlog

| Historia | Tareas principales |
|---|---|
| HU-03 | Diseñar pantalla de seguimiento, registrar gastos, calcular desvíos, mostrar alertas e historial. |
| HU-04 | Diseñar vista de informe, mostrar resumen por etapa, resaltar desvíos y preparar opción de descarga o impresión. |

### Incremento esperado

Al finalizar el Sprint 2, el usuario podrá:

- Registrar gastos reales por etapa.
- Consultar el avance físico y económico de la obra.
- Detectar etapas con desvíos de presupuesto.
- Generar un informe básico de presupuesto y ejecución.

---

# 9. Eventos Scrum

## Sprint Planning

Al inicio de cada Sprint, el Product Owner, el Scrum Master y el Equipo de Desarrollo revisarán el Product Backlog.

Durante la planificación se definirá:

- Qué historias tienen mayor prioridad.
- Qué historias puede completar el equipo según su capacidad.
- Cuál será el Sprint Goal.
- Qué tareas serán necesarias para completar cada historia.

---

## Daily Scrum

Se realizará una reunión diaria de hasta 15 minutos, en el mismo horario.

Cada integrante compartirá:

1. ¿Qué avancé desde el último Daily Scrum?
2. ¿En qué voy a trabajar antes del próximo Daily Scrum?
3. ¿Qué impedimentos o dificultades me están frenando?

Los impedimentos detectados serán gestionados por el Scrum Master junto con el equipo.

---

## Sprint Review

Al finalizar cada Sprint se presentará el incremento al Product Owner, al cliente o a los usuarios representativos.

Durante la revisión se verificará:

- Si las historias cumplen los criterios de aceptación.
- Si el incremento aporta valor al producto.
- Qué observaciones o cambios solicitan los usuarios.
- Qué elementos deben agregarse, modificarse o repriorizarse en el Product Backlog.

---

## Sprint Retrospective

Después de la Sprint Review, el equipo realizará una retrospectiva para analizar el proceso de trabajo.

Se responderán las siguientes preguntas:

- ¿Qué funcionó bien durante el Sprint?
- ¿Qué dificultades aparecieron?
- ¿Qué se puede mejorar en el próximo Sprint?
- ¿Qué acción concreta realizará el equipo para mejorar?

---

# 10. Definition of Ready

Una historia estará lista para ser seleccionada en un Sprint cuando:

- Tenga título y descripción en formato de historia de usuario.
- Esté priorizada por el Product Owner.
- Incluya criterios de aceptación claros y testeables.
- Tenga una estimación acordada por el Equipo de Desarrollo.
- No presente dependencias críticas sin resolver.
- El equipo comprenda su valor y alcance.

---

# 11. Definition of Done

Una historia se considerará terminada cuando:

- Todos sus criterios de aceptación se encuentren cumplidos.
- Las validaciones funcionales hayan sido realizadas.
- No existan defectos críticos pendientes.
- La funcionalidad esté integrada al incremento del Sprint.
- El tablero Scrum se encuentre actualizado.
- El Product Owner revise la historia durante la Sprint Review.
- La documentación mínima necesaria haya sido actualizada.

---

# 12. Tablero de trabajo propuesto

Para visualizar el avance se utilizará un tablero con tarjetas físicas, post-its o una herramienta digital.

| Product Backlog | Sprint Backlog | En progreso | En revisión | Terminado |
|---|---|---|---|---|
| Historias pendientes y priorizadas | Historias comprometidas para el Sprint | Tareas que se están desarrollando | Funcionalidades pendientes de prueba o validación | Historias que cumplen la Definition of Done |

Cada tarjeta debe incluir:

- Código de historia.
- Título.
- Descripción breve.
- Criterios de aceptación.
- Estimación en puntos.
- Prioridad.
- Sprint asignado.

---

# 13. Presentación ante la clase

Al finalizar la actividad, el equipo presentará:

1. El contexto del sistema PresuGalpón.
2. El problema que busca resolver para una empresa constructora.
3. El Product Goal.
4. Las cuatro historias de usuario elaboradas.
5. Los criterios de aceptación de cada historia.
6. La prioridad y estimación asignada a cada una.
7. El plan de Sprints propuesto.
8. El incremento esperado al finalizar cada Sprint.

La presentación deberá destacar que las historias no representan una especificación cerrada, sino elementos del Product Backlog que pueden refinarse mediante colaboración, revisión y feedback.

---

# 14. Gestión de feedback

Durante las presentaciones, las observaciones de otros equipos y del docente se registrarán como posibles ítems de mejora para el Product Backlog.

Ejemplos de feedback que podrían surgir:

- Incorporar diferentes tipos de galpones, como agrícolas, industriales o logísticos.
- Permitir cargar impuestos, descuentos o márgenes de ganancia.
- Agregar comparación entre proveedores de materiales.
- Incorporar gráficos de avance físico y financiero.
- Generar informes con mayor detalle para clientes.

Cada sugerencia deberá analizarse junto con el Product Owner para determinar:

- El valor que aporta al producto.
- La prioridad.
- El impacto sobre las historias existentes.
- La estimación necesaria.
- El Sprint en el que podría incorporarse.

---

# Conclusión

La aplicación de Scrum al sistema PresuGalpón permite organizar el trabajo de manera incremental, priorizando primero las funcionalidades que aportan mayor valor al negocio.

Las historias de usuario permiten expresar necesidades reales de los usuarios de forma clara, breve y verificable. A través de los Sprints, el equipo puede entregar incrementos funcionales, recibir feedback frecuente y adaptar el Product Backlog según las necesidades de la empresa constructora y de sus clientes.

De esta manera, Scrum facilita la colaboración, la transparencia, la inspección continua y la mejora del producto durante todo el desarrollo.
