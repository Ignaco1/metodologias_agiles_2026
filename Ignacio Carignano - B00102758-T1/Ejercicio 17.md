## Enunciado

### Objetivo

Desarrollar una aplicación web que permita a los usuarios gestionar sus finanzas personales de manera eficiente y segura.

La aplicación debe cumplir con los siguientes requisitos funcionales:

### 1. Gestión de cuentas bancarias

- Permitir la creación y edición de cuentas bancarias.
- Visualizar el saldo actual y el historial de movimientos de cada cuenta.
- Realizar transferencias entre cuentas propias.
- Descargar el historial de movimientos en formato CSV o PDF.

### 2. Gestión de ingresos y gastos

- Permitir la creación y edición de ingresos y gastos.
- Categorizar los ingresos y gastos por tipo, como salario, alquiler, alimentación, entre otros.
- Visualizar gráficos y reportes sobre los ingresos y gastos por categoría y período de tiempo.
- Establecer presupuestos para diferentes categorías de gastos.

### 3. Gestión de deudas

- Permitir la creación y edición de deudas.
- Indicar el monto total de la deuda, la tasa de interés, el plazo de pago y el monto de las cuotas.
- Visualizar un calendario de pagos y realizar simulaciones de diferentes escenarios de pago.
- Generar informes sobre el progreso en el pago de las deudas.

---

## Instrucciones para el alumno

1. **Identificar las interacciones funcionales:** analizar los requisitos funcionales descritos anteriormente e identificar todas las interacciones entre los usuarios y la aplicación.

2. **Clasificar las interacciones funcionales:** clasificar cada interacción funcional en una de las tres categorías de tamaño COSMIC: pequeña, mediana o grande.

3. **Calcular el tamaño funcional:** asignar un valor de Puntos de Función COSMIC (PFC) a cada interacción funcional en función de su clasificación de tamaño y sumar los valores para obtener el tamaño funcional total del proyecto en PFC.

4. **Obtener el costo por punto de función:** estimar el costo por punto de función considerando la complejidad del proyecto, el costo del equipo de desarrollo, gastos asociados y productividad histórica.

5. **Determinar la cantidad de PFC por mes:** estimar la cantidad de Puntos de Función COSMIC que un equipo de desarrollo de software puede desarrollar por mes, según su tamaño, experiencia y eficiencia.

6. **Calcular la duración del proyecto:** dividir el tamaño funcional total del proyecto entre la cantidad de PFC que se pueden desarrollar por mes.

7. **Estimar el costo total:** multiplicar el tamaño funcional total del proyecto por el costo por punto de función.

---

# Resolución

## 1. Introducción

Para estimar el tamaño funcional, la duración y el costo de la aplicación de gestión de finanzas personales se aplicará el método **COSMIC**.

COSMIC permite medir el tamaño funcional de un software a partir de los movimientos de datos que realiza para satisfacer los requisitos del usuario. Estos movimientos son:

- **Entrada (E):** datos que ingresan desde un usuario o sistema externo.
- **Lectura (R):** datos persistentes que el sistema consulta.
- **Escritura (W):** datos persistentes que el sistema crea, modifica o actualiza.
- **Salida (X):** datos que el sistema entrega al usuario o a un sistema externo.

Cada movimiento de datos identificado equivale a **1 Punto de Función COSMIC (CFP)**.

> **Aclaración metodológica:** la consigna solicita clasificar las interacciones como pequeñas, medianas o grandes. En esta resolución, esa clasificación se utiliza para expresar la complejidad relativa de cada proceso funcional. Sin embargo, el cálculo final se realiza siguiendo COSMIC: cada Entrada, Lectura, Escritura o Salida equivale a 1 CFP.

---

# 2. Estrategia de medición

## 2.1 Propósito de la medición

El propósito de esta medición es estimar:

- El tamaño funcional de la primera versión de la aplicación.
- El esfuerzo de desarrollo requerido.
- La duración aproximada del proyecto.
- El costo base de construcción del software.

---

## 2.2 Alcance de la medición

El alcance incluye las funcionalidades solicitadas en el enunciado:

- Gestión de cuentas bancarias.
- Gestión de ingresos y gastos.
- Gestión de presupuestos.
- Gestión de deudas.
- Generación de reportes, gráficos, simulaciones y exportaciones.

No se incluyen funcionalidades que no fueron solicitadas explícitamente, tales como:

- Registro e inicio de sesión de usuarios.
- Recuperación de contraseña.
- Notificaciones por correo o celular.
- Integración real con bancos.
- Integración con servicios de pago.
- Administración avanzada de usuarios.
- Aplicación móvil nativa.

Estas funcionalidades podrían incluirse en una futura versión y aumentarían el tamaño funcional total del proyecto.

---

## 2.3 Usuarios funcionales identificados

| Usuario funcional | Interacción principal con el sistema |
|---|---|
| Usuario de la aplicación | Crea y administra cuentas, ingresos, gastos, presupuestos y deudas. Consulta saldos, reportes, gráficos y calendarios. |
| Sistema de archivos | Recibe archivos CSV o PDF generados por la funcionalidad de exportación. |

---

## 2.4 Grupos de datos principales

| Grupo de datos | Descripción |
|---|---|
| Cuenta bancaria | Información de una cuenta personal: nombre, tipo, moneda, saldo y estado. |
| Movimiento bancario | Registro de ingresos, gastos, transferencias y otros movimientos asociados a una cuenta. |
| Categoría | Clasificación de ingresos y gastos, por ejemplo salario, alquiler, alimentación o transporte. |
| Presupuesto | Límite de gasto definido para una categoría en un período determinado. |
| Deuda | Información de una obligación financiera: monto, interés, plazo, cuotas y estado. |
| Pago de deuda | Registro de un pago realizado sobre una deuda. |
| Calendario de pagos | Información calculada de fechas, cuotas pendientes, vencimientos y proyecciones. |
| Reporte financiero | Resultado generado a partir de movimientos, categorías, presupuestos y deudas. |

---

# 3. Clasificación de tamaño utilizada

Para cumplir con la clasificación solicitada en la consigna, se utilizará la siguiente referencia:

| Clasificación | Cantidad de movimientos COSMIC | Interpretación |
|---|---:|---|
| Pequeña (S) | 3 a 4 CFP | Interacción simple, con pocos datos y operaciones persistentes. |
| Mediana (M) | 5 a 6 CFP | Interacción con validaciones, consultas o múltiples grupos de datos. |
| Grande (L) | 7 CFP o más | Interacción crítica o compleja, con varias lecturas, escrituras o validaciones. |

---

# 4. Identificación de procesos funcionales y movimientos COSMIC

## 4.1 Gestión de cuentas bancarias

| ID | Proceso funcional | Movimientos de datos identificados | Tamaño | CFP |
|---|---|---|---|---:|
| PF01 | Crear cuenta bancaria | E: ingresar datos de cuenta. W: guardar cuenta. X: confirmar creación. | S | 3 |
| PF02 | Editar cuenta bancaria | E: ingresar cambios. R: leer cuenta existente. W: actualizar cuenta. X: confirmar actualización. | S | 4 |
| PF03 | Consultar saldo e historial de movimientos | E: seleccionar cuenta y período. R: leer cuenta. R: leer movimientos. R: leer categorías. X: mostrar saldo e historial. | M | 5 |
| PF04 | Transferir fondos entre cuentas propias | E: ingresar cuenta origen, cuenta destino y monto. R: leer cuenta origen. R: leer cuenta destino. W: actualizar saldo origen. W: actualizar saldo destino. W: registrar transferencia. X: confirmar transferencia. | L | 7 |
| PF05 | Descargar historial de movimientos en CSV o PDF | E: seleccionar cuenta, período y formato. R: leer cuenta. R: leer movimientos. X: generar archivo descargable. | S | 4 |

### Subtotal del módulo de cuentas bancarias

| Módulo | CFP |
|---|---:|
| Gestión de cuentas bancarias | **23 CFP** |

---

## 4.2 Gestión de ingresos, gastos y presupuestos

| ID | Proceso funcional | Movimientos de datos identificados | Tamaño | CFP |
|---|---|---|---|---:|
| PF06 | Crear o editar ingreso o gasto | E: ingresar datos del movimiento. R: leer cuenta asociada. R: leer categoría. W: guardar o actualizar movimiento. X: confirmar operación. | M | 5 |
| PF07 | Consultar gráficos y reportes de ingresos y gastos | E: seleccionar período, cuenta o categoría. R: leer movimientos. R: leer categorías. R: leer presupuestos. X: mostrar gráficos y reportes. | M | 5 |
| PF08 | Establecer presupuesto por categoría | E: ingresar categoría, período y monto límite. R: leer categoría. R: leer gastos actuales. W: guardar presupuesto. X: confirmar presupuesto y mostrar estado. | M | 5 |

> La categorización de ingresos y gastos se incluye dentro del proceso **PF06**, ya que al crear o editar un movimiento el usuario debe seleccionar una categoría.

### Subtotal del módulo de ingresos, gastos y presupuestos

| Módulo | CFP |
|---|---:|
| Gestión de ingresos, gastos y presupuestos | **15 CFP** |

---

## 4.3 Gestión de deudas

| ID | Proceso funcional | Movimientos de datos identificados | Tamaño | CFP |
|---|---|---|---|---:|
| PF09 | Crear o editar deuda | E: ingresar monto, tasa, plazo y cuotas. R: leer deuda existente cuando corresponde editar. W: guardar o actualizar deuda. W: generar o actualizar plan de cuotas. X: confirmar operación. | M | 5 |
| PF10 | Registrar pago de deuda | E: ingresar datos del pago. R: leer deuda asociada. W: guardar pago. W: actualizar saldo o estado de la deuda. X: confirmar pago registrado. | M | 5 |
| PF11 | Consultar calendario de pagos y simular escenarios | E: seleccionar deuda y condiciones de simulación. R: leer deuda. R: leer cuotas programadas. R: leer pagos realizados. X: mostrar calendario. X: mostrar simulación proyectada. | M | 6 |
| PF12 | Generar informe de progreso de pago de deudas | E: seleccionar deuda o período. R: leer deuda. R: leer cuotas programadas. R: leer pagos realizados. X: mostrar informe de progreso. | M | 5 |

### Subtotal del módulo de deudas

| Módulo | CFP |
|---|---:|
| Gestión de deudas | **21 CFP** |

---

# 5. Tamaño funcional total del proyecto

## 5.1 Resumen por módulo

| Módulo funcional | CFP |
|---|---:|
| Gestión de cuentas bancarias | 23 CFP |
| Gestión de ingresos, gastos y presupuestos | 15 CFP |
| Gestión de deudas | 21 CFP |
| **Tamaño funcional total** | **59 CFP** |

Por lo tanto, el tamaño funcional estimado de la aplicación es:

> **X = 59 Puntos de Función COSMIC (CFP)**

---

# 6. Estimación del costo por punto de función

## 6.1 Equipo de trabajo estimado

Para realizar la estimación se propone un equipo de **5 personas**.

| Rol | Cantidad | Costo mensual estimado por persona | Costo mensual total |
|---|---:|---:|---:|
| Líder de proyecto / Analista funcional | 1 | USD 3.500 | USD 3.500 |
| Desarrollador Full Stack | 2 | USD 3.800 | USD 7.600 |
| QA / Tester | 1 | USD 2.700 | USD 2.700 |
| Diseñador UX/UI y apoyo DevOps | 1 | USD 2.300 | USD 2.300 |
| **Subtotal de remuneraciones** | **5** |  | **USD 16.100** |

Además de las remuneraciones, se consideran costos indirectos de infraestructura, herramientas, licencias, administración, gestión, pruebas, seguros y contingencias operativas.

| Concepto adicional | Costo mensual estimado |
|---|---:|
| Infraestructura, servicios cloud, herramientas y licencias | USD 1.500 |
| Administración, gestión, beneficios y costos indirectos | USD 2.200 |
| **Total de costos indirectos** | **USD 3.700** |

### Costo mensual total del equipo

| Concepto | Valor |
|---|---:|
| Subtotal de remuneraciones | USD 16.100 |
| Costos indirectos | USD 3.700 |
| **Costo mensual total del equipo** | **USD 19.800** |

> **Nota:** los valores se utilizan como supuesto académico de estimación, siguiendo el ejemplo de productividad y costo mensual presentado en el material de clase. No representan una cotización comercial definitiva.

---

## 6.2 Productividad estimada

De acuerdo con el ejemplo utilizado en el material de la cátedra, se toma una productividad histórica de:

> **W = 23 CFP por mes**

Esta productividad se refiere a puntos de función completamente desarrollados, probados e instalados en un entorno de producción.

---

## 6.3 Cálculo del costo por punto de función

La fórmula aplicada es:

```text
Costo por Punto de Función = Costo mensual total del equipo / Productividad mensual
```

Reemplazando los valores:

```text
CPFC = USD 19.800 / 23 CFP
CPFC = USD 860,87 por CFP
```

Por lo tanto:

> **Y = USD 860,87 por Punto de Función COSMIC**

---

# 7. Cálculo de la duración del proyecto

La fórmula aplicada es:

```text
Duración del proyecto = Tamaño funcional total / Productividad mensual
```

Reemplazando los valores:

```text
Duración = 59 CFP / 23 CFP por mes
Duración = 2,57 meses
```

Por lo tanto:

> **A = 2,57 meses**

La duración estimada equivale aproximadamente a:

- 2 meses y medio de desarrollo.
- Cerca de 11 semanas de trabajo.
- 3 iteraciones de desarrollo de aproximadamente 4 semanas, incluyendo análisis, pruebas y correcciones.

---

# 8. Cálculo del costo total del proyecto

La fórmula aplicada es:

```text
Costo total del proyecto = Tamaño funcional total × Costo por Punto de Función
```

Reemplazando los valores:

```text
Costo total = 59 CFP × USD 860,87 por CFP
Costo total = USD 50.791,30
```

Por lo tanto:

> **B = USD 50.791,30**

---

# 9. Resumen final de la estimación

| Variable | Descripción | Resultado |
|---|---|---:|
| X | Tamaño funcional total del proyecto | **59 CFP** |
| Y | Costo por Punto de Función COSMIC | **USD 860,87 por CFP** |
| Z | Cantidad de integrantes del equipo | **5 personas** |
| W | Productividad estimada del equipo | **23 CFP por mes** |
| A | Duración estimada del proyecto | **2,57 meses** |
| B | Costo total estimado del proyecto | **USD 50.791,30** |

---

# 10. Presupuesto recomendado con contingencia

Aunque la consigna solicita el costo base del proyecto, en un escenario real conviene reservar una contingencia para riesgos, cambios de alcance, defectos no previstos, demoras de integración o ajustes solicitados por los usuarios.

Se propone una contingencia del 10%.

```text
Contingencia = USD 50.791,30 × 10%
Contingencia = USD 5.079,13
```

```text
Presupuesto recomendado = Costo base + Contingencia
Presupuesto recomendado = USD 50.791,30 + USD 5.079,13
Presupuesto recomendado = USD 55.870,43
```

| Concepto | Monto |
|---|---:|
| Costo base estimado | USD 50.791,30 |
| Contingencia recomendada del 10% | USD 5.079,13 |
| **Presupuesto recomendado** | **USD 55.870,43** |

> La contingencia no modifica el valor B solicitado por la consigna. El costo base del proyecto sigue siendo USD 50.791,30.

---

# 11. Conclusión

La aplicación de gestión de finanzas personales presenta un tamaño funcional estimado de **59 Puntos de Función COSMIC**.

La funcionalidad de mayor tamaño es la transferencia entre cuentas propias, ya que requiere validar la cuenta origen y destino, actualizar ambos saldos, registrar el movimiento y confirmar la operación al usuario.

A partir de una productividad estimada de **23 CFP por mes** y un costo mensual total del equipo de **USD 19.800**, se obtiene un costo por punto de función de **USD 860,87**.

Con estos valores, se estima que el proyecto:

- Requerirá aproximadamente **2,57 meses** de trabajo.
- Tendrá un costo base de **USD 50.791,30**.
- Podría requerir un presupuesto recomendado de **USD 55.870,43** al considerar una contingencia del 10%.

La estimación permite planificar recursos, tiempo y costo de forma estructurada. Sin embargo, los valores deben revisarse si cambian los requisitos funcionales, la composición del equipo, la productividad histórica o el alcance del proyecto.

---

# Bibliografía utilizada

- Material de clase: **Estimación de Costos – Método COSMIC**.
- COSMIC. *Manual de medición COSMIC para ISO 19761. Parte 1: Principios, Definiciones y Reglas. Versión 5.0*.
- COSMIC. *COSMIC Software Sizing – Open Standard for Software Size Measurement*.
- Recursos complementarios proporcionados por la cátedra.
```
