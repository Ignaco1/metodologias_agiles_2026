## Enunciado

### Objetivo

Utilizar el método Delphi para llegar a un consenso sobre la tecnología y la arquitectura más adecuadas para el desarrollo de una billetera virtual segura, escalable y confiable.

### Descripción

El método Delphi es una técnica de consulta estructurada que se utiliza para obtener opiniones expertas sobre un tema complejo. En este caso, el método Delphi se utilizará para recopilar información y opiniones de expertos en blockchain, seguridad, desarrollo de software y arquitectura de sistemas sobre la mejor tecnología y arquitectura para una billetera virtual.

---

### 1. Definición del problema

- Describir claramente los objetivos y requisitos de la billetera virtual, tal como se presentó en el enunciado anterior.
- Identificar los factores clave que se deben considerar al seleccionar la tecnología y la arquitectura, como la seguridad, la escalabilidad, la confiabilidad, la facilidad de uso y el costo.

### 2. Selección del panel de expertos

- Identificar y reclutar a un grupo de expertos con experiencia en las áreas relevantes, como blockchain, seguridad, desarrollo de software y arquitectura de sistemas.
- El panel de expertos debe estar compuesto por individuos con diferentes perspectivas y experiencias para garantizar la diversidad de opiniones.
- Es importante que los expertos sean independientes y no tengan conflictos de intereses.

### 3. Elaboración del cuestionario

- Diseñar un cuestionario que presente a los expertos una lista de opciones de tecnología y arquitectura para la billetera virtual.
- El cuestionario debe incluir preguntas que permitan a los expertos evaluar cada opción en función de los factores clave identificados en el paso 1.
- Las preguntas pueden ser de tipo Likert, abiertas o una combinación de ambas.

### 4. Aplicación del método Delphi

- Distribuir el cuestionario a los expertos de forma anónima.
- Recopilar las respuestas de los expertos y analizarlas estadísticamente.
- Sintetizar los resultados y presentarlos al panel de expertos.
- Brindar a los expertos la oportunidad de revisar y comentar los resultados.
- Realizar una segunda ronda de cuestionarios, incorporando los comentarios de la primera ronda.
- Analizar nuevamente las respuestas y presentar los resultados finales al panel de expertos.

### 5. Selección de la tecnología y la arquitectura

- Con base en los resultados del método Delphi, seleccionar la tecnología y la arquitectura que mejor se adapten a los objetivos y requisitos de la billetera virtual.
- Justificar la selección de la tecnología y la arquitectura elegidas, considerando los aportes del panel de expertos y los resultados del análisis estadístico.

### 6. Documentación y comunicación

- Documentar cuidadosamente el proceso de toma de decisiones, incluyendo los criterios utilizados, las opciones consideradas y la justificación de la selección final.
- Comunicar la decisión tomada a las partes interesadas, incluyendo a los desarrolladores, inversores y usuarios potenciales.

---

# Resolución

## Introducción

Para resolver este ejercicio se aplicará el Método Delphi como una técnica de consulta estructurada, iterativa y anónima. El objetivo será obtener un consenso informado sobre la tecnología y la arquitectura más adecuadas para desarrollar una billetera virtual.

La resolución se presenta como una **simulación académica**. Por lo tanto, los expertos, las respuestas, las puntuaciones y los resultados del consenso son hipotéticos, pero fueron construidos respetando el proceso propio del método Delphi: definición del problema, selección del panel, cuestionarios, rondas de consulta, análisis, consenso y documentación de la decisión.

El método Delphi resulta adecuado para este caso porque la elección tecnológica de una billetera virtual involucra decisiones complejas relacionadas con seguridad, escalabilidad, confiabilidad, costos, experiencia de usuario, integración con servicios externos y mantenimiento futuro.

---

# 1. Definición del problema

## 1.1 Contexto de la billetera virtual

Se propone desarrollar una aplicación denominada **BilleteraSegura**, una billetera virtual destinada a usuarios que necesitan consultar su saldo, cargar fondos mediante proveedores autorizados, realizar transferencias entre usuarios, revisar movimientos y recibir notificaciones de sus operaciones.

El sistema debe ofrecer una experiencia clara para el usuario, pero al mismo tiempo debe mantener la seguridad, la integridad de las transacciones y la trazabilidad de cada operación.

La billetera virtual no debe ser entendida únicamente como una aplicación de interfaz. Debe incluir una arquitectura capaz de administrar identidades, permisos, saldos, movimientos, auditorías, alertas y posibles integraciones con proveedores de pago.

---

## 1.2 Objetivo del sistema

El objetivo de BilleteraSegura es permitir a los usuarios administrar fondos virtuales de manera segura, confiable y trazable.

La primera versión del producto deberá permitir:

- Crear una cuenta de usuario.
- Iniciar sesión de forma segura.
- Consultar el saldo disponible.
- Cargar fondos mediante una integración externa autorizada.
- Transferir fondos entre usuarios registrados.
- Consultar el historial de movimientos.
- Recibir notificaciones ante operaciones relevantes.
- Bloquear temporalmente una cuenta ante actividad sospechosa.
- Mantener un registro auditable de todas las transacciones.

---

## 1.3 Requisitos funcionales

| Código | Requisito funcional |
|---|---|
| RF01 | El sistema debe permitir registrar una cuenta de billetera virtual asociada a un usuario. |
| RF02 | El sistema debe permitir iniciar y cerrar sesión de forma segura. |
| RF03 | El sistema debe permitir consultar el saldo disponible de la cuenta. |
| RF04 | El sistema debe permitir cargar fondos mediante un proveedor de pagos autorizado. |
| RF05 | El sistema debe permitir realizar transferencias entre cuentas de usuarios existentes. |
| RF06 | El sistema debe permitir consultar el historial de movimientos de la cuenta. |
| RF07 | El sistema debe enviar notificaciones ante cargas, transferencias, rechazos o bloqueos. |
| RF08 | El sistema debe permitir bloquear o desbloquear una cuenta por motivos de seguridad. |
| RF09 | El sistema debe registrar trazabilidad y auditoría de las operaciones críticas. |
| RF10 | El sistema debe permitir a un administrador revisar operaciones marcadas como sospechosas. |

---

## 1.4 Requisitos no funcionales

| Código | Requisito no funcional |
|---|---|
| RNF01 | La aplicación debe proteger el acceso mediante autenticación robusta y segundo factor de verificación. |
| RNF02 | Las comunicaciones entre cliente, API y servicios externos deben utilizar canales cifrados. |
| RNF03 | La arquitectura debe asegurar que una transferencia no genere saldos inconsistentes. |
| RNF04 | El sistema debe poder crecer en cantidad de usuarios y operaciones sin requerir una reconstrucción completa. |
| RNF05 | El sistema debe contar con monitoreo, registros de auditoría, copias de seguridad y recuperación ante fallas. |
| RNF06 | La interfaz debe ser clara para usuarios no técnicos y permitir comprender el estado de cada operación. |
| RNF07 | La solución debe evitar costos técnicos innecesarios durante la primera versión del producto. |
| RNF08 | El diseño debe facilitar mantenimiento, pruebas, cambios futuros e integración con proveedores externos. |
| RNF09 | La información sensible debe almacenarse minimizando exposición y aplicando controles de acceso. |

---

## 1.5 Factores clave para la toma de decisión

Para seleccionar la tecnología y la arquitectura se definieron los siguientes factores de evaluación:

| Factor | Descripción | Peso asignado |
|---|---|---:|
| Seguridad | Protección de identidad, fondos, datos sensibles, permisos y operaciones. | 25% |
| Confiabilidad e integridad | Capacidad de evitar inconsistencias, pérdidas de información o transacciones incompletas. | 20% |
| Escalabilidad | Capacidad de atender un crecimiento de usuarios y operaciones. | 15% |
| Trazabilidad y auditoría | Registro verificable de movimientos, decisiones y eventos de seguridad. | 15% |
| Costo | Costo de desarrollo, infraestructura, mantenimiento y operación. | 10% |
| Mantenibilidad | Facilidad para corregir, probar, evolucionar e integrar nuevos módulos. | 10% |
| Facilidad de uso | Capacidad de ofrecer una experiencia clara, rápida y comprensible. | 5% |

Los factores de seguridad, confiabilidad y trazabilidad tienen mayor peso porque una falla en estas dimensiones puede afectar directamente los fondos, la confianza de los usuarios y la viabilidad del producto.

---

# 2. Selección del panel de expertos

## 2.1 Moderador y grupo de control

Se designa un **moderador Delphi** encargado de:

- Preparar los cuestionarios.
- Mantener el anonimato de los participantes.
- Distribuir y recopilar las respuestas.
- Sintetizar los resultados de cada ronda.
- Presentar las conclusiones sin modificar la opinión individual de los expertos.
- Documentar el proceso completo.

Además, se propone un **grupo de control** formado por integrantes del equipo del proyecto. Su función será revisar que el cuestionario sea comprensible, que las opciones tecnológicas estén correctamente definidas y que los resultados sean comunicados de forma clara.

El grupo de control no participa en las votaciones del panel de expertos.

---

## 2.2 Composición del panel

Se propone un panel de diez expertos independientes. Para preservar el anonimato, se identifican mediante códigos.

| Código | Perfil del experto | Aporte esperado |
|---|---|---|
| E01 | Arquitecto de software | Evalúa la estructura general, separación de responsabilidades y evolución futura. |
| E02 | Especialista en ciberseguridad | Evalúa autenticación, cifrado, control de acceso, amenazas y auditoría. |
| E03 | Desarrollador backend fintech | Evalúa APIs, reglas de negocio, transacciones y consistencia de saldos. |
| E04 | Especialista en cloud y DevOps | Evalúa despliegue, escalabilidad, monitoreo, disponibilidad y costos operativos. |
| E05 | Experto en blockchain | Evalúa el aporte real de blockchain, trazabilidad distribuida y costos de adopción. |
| E06 | Especialista en bases de datos | Evalúa persistencia, integridad transaccional, respaldo y recuperación. |
| E07 | Responsable de cumplimiento y riesgos | Evalúa auditoría, protección de información y gestión de riesgos. |
| E08 | Diseñador UX/UI | Evalúa facilidad de uso, comprensión de movimientos y prevención de errores del usuario. |
| E09 | Analista de producto digital | Evalúa valor de negocio, viabilidad del MVP y priorización. |
| E10 | QA y analista de calidad | Evalúa pruebas, confiabilidad, criterios de aceptación y escenarios de fallo. |

---

## 2.3 Criterios de selección del panel

Los integrantes del panel deben cumplir los siguientes criterios:

- Tener experiencia comprobable en su área de especialización.
- Poder analizar el problema desde una perspectiva técnica, de negocio, seguridad, operación o experiencia de usuario.
- No poseer conflictos de interés con proveedores tecnológicos específicos.
- Comprometerse a participar en las rondas definidas.
- Aceptar que sus respuestas serán anónimas frente al resto de los expertos.
- Fundamentar sus respuestas cuando se alejen de la tendencia general.

La diversidad del panel permite evitar una decisión tomada desde una única perspectiva. Por ejemplo, una tecnología puede parecer atractiva desde el punto de vista técnico, pero resultar costosa, difícil de mantener o poco conveniente para el usuario final.

---

# 3. Elaboración del cuestionario

## 3.1 Opciones tecnológicas y arquitectónicas evaluadas

Se presentan al panel cuatro alternativas para la primera versión de BilleteraSegura.

| Opción | Tecnología y arquitectura propuesta |
|---|---|
| Opción A | Monolito modular en capas: frontend web responsive, API REST en ASP.NET Core, PostgreSQL, Redis, Docker y despliegue cloud. |
| Opción B | Arquitectura de microservicios: servicios independientes para identidad, billetera, transferencias, notificaciones y auditoría; base de datos por servicio y mensajería asíncrona. |
| Opción C | Arquitectura blockchain-first: uso de blockchain privada como núcleo del registro de transacciones, junto con servicios de aplicación y contratos inteligentes. |
| Opción D | Arquitectura serverless: funciones en la nube, base de datos administrada, eventos asíncronos y servicios gestionados para escalar bajo demanda. |

---

## 3.2 Instrumento de evaluación

El cuestionario combina preguntas cerradas de escala Likert con preguntas abiertas.

Para las preguntas cerradas se utiliza la siguiente escala:

| Puntuación | Significado |
|---:|---|
| 1 | Muy desfavorable |
| 2 | Desfavorable |
| 3 | Aceptable |
| 4 | Favorable |
| 5 | Muy favorable |

---

## 3.3 Preguntas cerradas

Cada experto debe evaluar cada opción tecnológica según los siguientes criterios:

1. ¿Qué tan adecuada considera esta opción para proteger cuentas, datos sensibles y transacciones?
2. ¿Qué tan adecuada considera esta opción para asegurar la integridad de saldos y movimientos?
3. ¿Qué tan adecuada considera esta opción para escalar ante un crecimiento de usuarios y operaciones?
4. ¿Qué tan adecuada considera esta opción para mantener registros auditables y trazables?
5. ¿Qué tan adecuada considera esta opción para mantener costos razonables durante un MVP?
6. ¿Qué tan fácil considera que será mantener y evolucionar esta opción?
7. ¿Qué tan adecuada considera esta opción para integrarse con proveedores externos de pago?
8. ¿Qué tan adecuada considera esta opción para ofrecer una experiencia clara y rápida al usuario?
9. ¿Qué nivel de riesgo técnico presenta esta opción?
10. ¿Recomendaría seleccionar esta opción como arquitectura principal del MVP?

---

## 3.4 Preguntas abiertas

Además de las preguntas cerradas, cada experto debe responder:

1. ¿Cuál considera que es el mayor riesgo de seguridad para una billetera virtual?
2. ¿Qué controles mínimos deberían existir antes de permitir transferencias entre usuarios?
3. ¿En qué situación considera justificable usar blockchain como parte de la solución?
4. ¿Qué riesgos aparecen al implementar microservicios desde el inicio del producto?
5. ¿Qué componentes deberían mantenerse separados dentro de la arquitectura?
6. ¿Qué indicadores deberían monitorearse durante la operación de la billetera?
7. ¿Qué alternativa considera más adecuada para el MVP y por qué?
8. ¿Qué cambios recomienda realizar sobre las opciones propuestas?

---

## 3.5 Criterio de consenso

Para este ejercicio se establece que existe consenso cuando:

- Al menos el 80% de los expertos puntúa una propuesta con 4 o 5 en la recomendación final.
- La mediana de la opción es igual o superior a 4.
- La dispersión de las respuestas es baja o moderada.
- Las observaciones abiertas no revelan riesgos críticos sin mitigación.

---

# 4. Aplicación del Método Delphi

## 4.1 Primera ronda

En la primera ronda se distribuye el cuestionario de forma individual y anónima.

Cada experto evalúa las cuatro opciones y responde las preguntas abiertas. El moderador recopila las respuestas, calcula medianas, identifica niveles de acuerdo y resume los argumentos principales.

### Resultados simulados de la primera ronda

| Opción | Seguridad | Confiabilidad | Escalabilidad | Costo | Mantenibilidad | Recomendación general |
|---|---:|---:|---:|---:|---:|---:|
| Opción A – Monolito modular | 5 | 5 | 4 | 5 | 5 | 4,6 |
| Opción B – Microservicios | 4 | 4 | 5 | 2 | 3 | 3,7 |
| Opción C – Blockchain-first | 3 | 3 | 3 | 2 | 2 | 2,8 |
| Opción D – Serverless | 4 | 4 | 5 | 4 | 4 | 4,1 |

### Síntesis de opiniones de la primera ronda

Los expertos valoran positivamente la Opción A porque:

- Permite implementar controles de seguridad e integridad de manera centralizada.
- Reduce la complejidad inicial respecto de microservicios.
- Facilita el desarrollo, las pruebas y la auditoría del MVP.
- Resulta más simple de mantener para un equipo pequeño o mediano.
- Permite evolucionar a servicios independientes si el crecimiento futuro lo justifica.

La Opción B recibe una valoración favorable en escalabilidad, pero varios expertos consideran que iniciar con microservicios podría generar:

- Mayor complejidad operativa.
- Más puntos de fallo.
- Mayor costo de infraestructura.
- Necesidad de un equipo con experiencia especializada en observabilidad, mensajería y despliegue distribuido.

La Opción C genera desacuerdo. Los expertos coinciden en que blockchain puede aportar valor en escenarios específicos de trazabilidad compartida entre múltiples organizaciones, pero no consideran que sea necesaria como núcleo de un MVP de billetera virtual.

La Opción D obtiene buena valoración por escalabilidad y servicios administrados. Sin embargo, los expertos señalan que las operaciones financieras críticas requieren especial atención en consistencia, trazabilidad y control transaccional.

---

## 4.2 Síntesis enviada al panel

El moderador envía a cada experto un resumen anónimo con:

- Medianas de las puntuaciones.
- Nivel de acuerdo alcanzado.
- Riesgos señalados por el panel.
- Argumentos principales a favor y en contra de cada opción.
- Preguntas específicas para revisar en la segunda ronda.

El resumen aclara que la Opción A fue la alternativa con mayor apoyo inicial, mientras que la Opción D podría utilizarse de forma complementaria para componentes no críticos, como notificaciones, procesamiento diferido o reportes.

---

## 4.3 Segunda ronda

En la segunda ronda, los expertos revisan el resumen de resultados y vuelven a responder sobre las decisiones principales.

### Preguntas de segunda ronda

1. ¿Está de acuerdo con que la arquitectura principal del MVP sea un monolito modular en capas?
2. ¿Está de acuerdo con utilizar una base de datos relacional con transacciones para proteger la consistencia de saldos y movimientos?
3. ¿Está de acuerdo con postergar una arquitectura de microservicios hasta que existan métricas reales de crecimiento?
4. ¿Está de acuerdo con no utilizar blockchain como componente central del MVP?
5. ¿Está de acuerdo con utilizar componentes asíncronos o serverless únicamente para tareas no críticas?
6. ¿Está de acuerdo con establecer autenticación multifactor, auditoría y monitoreo como requisitos obligatorios del producto?

---

## 4.4 Resultados simulados de la segunda ronda

| Declaración evaluada | Acuerdo del panel | Resultado |
|---|---:|---|
| Usar una arquitectura de monolito modular para el MVP. | 90% | Consenso alcanzado. |
| Usar una base de datos relacional con transacciones. | 100% | Consenso alcanzado. |
| Postergar microservicios hasta que el crecimiento lo justifique. | 90% | Consenso alcanzado. |
| No usar blockchain como núcleo del MVP. | 80% | Consenso alcanzado. |
| Usar procesos asíncronos solo para tareas no críticas. | 90% | Consenso alcanzado. |
| Aplicar autenticación multifactor, auditoría y monitoreo desde la primera versión. | 100% | Consenso alcanzado. |

---

## 4.5 Conclusión del proceso Delphi

Luego de dos rondas se alcanza un consenso suficiente.

La tecnología y arquitectura recomendadas para BilleteraSegura son:

> Una arquitectura de **monolito modular en capas**, desplegada en la nube, con una API segura, base de datos relacional transaccional, módulos independientes por responsabilidad y componentes asíncronos solo para operaciones no críticas.

La arquitectura de microservicios se considera una alternativa futura, no una decisión inicial.

Blockchain se mantiene como una posibilidad para una etapa posterior, únicamente si el producto necesita compartir una trazabilidad inmutable entre entidades independientes y existe una justificación real de negocio, técnica y económica.

---

# 5. Selección de la tecnología y la arquitectura

## 5.1 Decisión final

La solución seleccionada para el MVP de BilleteraSegura será la siguiente:

| Componente | Tecnología o enfoque seleccionado |
|---|---|
| Cliente | Aplicación web responsive o PWA para operar desde computadoras y dispositivos móviles. |
| Backend | API REST desarrollada con ASP.NET Core. |
| Arquitectura | Monolito modular con separación por capas y responsabilidades. |
| Dominio | Módulos de identidad, billetera, transferencias, auditoría, notificaciones y administración. |
| Persistencia | Base de datos relacional PostgreSQL. |
| Caché y protección | Redis para caché, control de frecuencia y operaciones temporales. |
| Integridad transaccional | Transacciones de base de datos para asegurar que los movimientos se confirmen o reviertan en conjunto. |
| Procesos asíncronos | Cola de eventos para notificaciones, alertas y tareas no críticas. |
| Despliegue | Contenedores Docker sobre infraestructura cloud. |
| Seguridad | HTTPS, autenticación multifactor, permisos por rol, registros de auditoría y monitoreo. |
| Blockchain | No se incorpora como núcleo del MVP; queda sujeto a análisis futuro. |

---

## 5.2 Arquitectura propuesta

flowchart LR
  U[Usuario] --> C[Cliente Web Responsive / PWA]
  C --> API[API REST]

  API --> AUTH[Módulo de Identidad y Seguridad]
  API --> WALLET[Módulo de Billetera y Transferencias]
  API --> AUDIT[Módulo de Auditoría]
  API --> NOTIF[Módulo de Notificaciones]
  API --> ADMIN[Módulo de Administración]

  WALLET --> DB[(PostgreSQL)]
  AUTH --> DB
  AUDIT --> DB
  ADMIN --> DB

  API --> CACHE[(Redis)]
  NOTIF --> QUEUE[Cola de eventos]
  QUEUE --> WORKER[Procesador asíncrono]
  WORKER --> MSG[Correo / Notificación push]

  API --> PAY[Proveedor externo de pagos]


## 5.3 Justificación de la selección

La arquitectura seleccionada responde a los factores más valorados por el panel de expertos.

### Seguridad

La solución permite centralizar autenticación, permisos, auditoría y validaciones críticas dentro del backend.

Las transferencias no deben depender de la lógica del cliente. La API debe validar identidad, autorización, saldo disponible, límites de operación y consistencia de la transacción antes de modificar cualquier saldo.

### Confiabilidad e integridad

La base de datos relacional permite utilizar transacciones para proteger operaciones críticas.

Por ejemplo, una transferencia debe garantizar que:

1. Se descuente el saldo de la cuenta origen.
2. Se incremente el saldo de la cuenta destino.
3. Se registren ambos movimientos.
4. Se genere un evento de auditoría.
5. Si alguna de estas acciones falla, toda la operación se revierta.

### Escalabilidad

La arquitectura modular permite evolucionar progresivamente.

Si el crecimiento de usuarios, transferencias o notificaciones lo justifica, algunos módulos pueden separarse en servicios independientes. Por ejemplo, notificaciones, reportes o procesamiento de alertas pueden evolucionar sin necesidad de dividir toda la aplicación desde el inicio.

### Costo y mantenibilidad

Un monolito modular reduce la complejidad inicial de desarrollo, despliegue, monitoreo y pruebas.

La solución evita adoptar herramientas distribuidas complejas antes de que exista una necesidad real. Esto permite concentrar recursos en la calidad del producto, los controles de seguridad y la validación con usuarios.

### Blockchain

El panel considera que blockchain no debe utilizarse por moda o como requisito automático.

Podría analizarse en una evolución futura si se requiere compartir información verificable entre bancos, entidades financieras, comercios, organismos regulatorios u otras organizaciones independientes.

Para el MVP, una base de datos relacional, transacciones, auditoría y controles de seguridad cubren de manera más directa las necesidades principales del producto.

---

## 5.4 Controles de seguridad mínimos

La solución seleccionada debe incorporar como mínimo:

- Autenticación multifactor.
- Almacenamiento seguro de credenciales.
- Comunicaciones cifradas mediante HTTPS.
- Control de permisos por roles.
- Límite de intentos de inicio de sesión.
- Registro de auditoría de operaciones críticas.
- Detección de actividad inusual.
- Validación de saldo antes de una transferencia.
- Idempotencia para evitar duplicar operaciones ante reintentos.
- Copias de seguridad periódicas.
- Monitoreo de disponibilidad, errores y tiempos de respuesta.
- Pruebas de seguridad, integración y recuperación ante fallas.

---

# 6. Documentación y comunicación

## 6.1 Documento de decisión tecnológica

La decisión final deberá quedar registrada en un documento de arquitectura que incluya:

- Contexto de la billetera virtual.
- Objetivos del producto.
- Requisitos funcionales y no funcionales.
- Factores de evaluación.
- Composición y criterios del panel de expertos.
- Opciones tecnológicas consideradas.
- Cuestionarios aplicados.
- Resultados de cada ronda.
- Criterio de consenso utilizado.
- Arquitectura seleccionada.
- Riesgos identificados y mitigaciones.
- Decisiones postergadas para futuras versiones.
- Plan de revisión de la arquitectura.

---

## 6.2 Registro de riesgos

| ID | Riesgo | Impacto | Mitigación propuesta |
|---|---|---:|---|
| R01 | Transferencia duplicada por reintento de red. | Alto | Usar identificadores únicos e idempotencia en las operaciones. |
| R02 | Saldo inconsistente entre origen y destino. | Alto | Ejecutar transferencias dentro de una transacción. |
| R03 | Acceso no autorizado a una cuenta. | Alto | Aplicar autenticación multifactor, permisos y monitoreo. |
| R04 | Crecimiento de operaciones superior a lo esperado. | Medio | Diseñar módulos desacoplados y monitorear métricas de rendimiento. |
| R05 | Costos de infraestructura elevados. | Medio | Priorizar componentes administrados solo donde aporten valor y revisar consumo periódicamente. |
| R06 | Dependencia excesiva de un proveedor externo. | Medio | Diseñar integraciones mediante interfaces y adaptadores. |
| R07 | Complejidad excesiva por adoptar blockchain o microservicios antes de tiempo. | Alto | Mantener la solución inicial simple y evaluar cambios con métricas reales. |

---

## 6.3 Comunicación a las partes interesadas

La decisión se comunicará a cada grupo de interés de la siguiente manera:

| Parte interesada | Información a comunicar |
|---|---|
| Equipo de desarrollo | Arquitectura seleccionada, módulos, estándares de seguridad, responsabilidades técnicas y plan de implementación. |
| Inversores o responsables de negocio | Justificación de costos, riesgos, escalabilidad progresiva y alcance del MVP. |
| Usuarios potenciales | Funcionalidades disponibles, protección de cuenta, límites operativos y canales de soporte. |
| Equipo de QA | Criterios de aceptación, escenarios críticos, pruebas de seguridad, integración y recuperación. |
| Operaciones y DevOps | Requisitos de despliegue, monitoreo, respaldo, alertas y plan de recuperación. |
| Responsables de cumplimiento | Evidencias de trazabilidad, auditoría, permisos y tratamiento de información sensible. |

---

# 7. Plan de seguimiento

La arquitectura elegida deberá revisarse periódicamente.

Se propone evaluar los siguientes indicadores:

- Cantidad de usuarios activos.
- Cantidad de transferencias por día.
- Tiempo promedio de respuesta de la API.
- Tasa de errores por operación.
- Cantidad de operaciones rechazadas por seguridad.
- Disponibilidad del sistema.
- Tiempo de recuperación ante fallas.
- Costo mensual de infraestructura.
- Cantidad de incidentes de auditoría.
- Satisfacción de los usuarios.

Si los indicadores muestran que la solución inicial no puede responder adecuadamente al crecimiento, se realizará una nueva evaluación Delphi o una revisión arquitectónica para decidir qué módulos conviene separar o rediseñar.

---

# Conclusión

El Método Delphi permitió estructurar la decisión sobre la tecnología y arquitectura de una billetera virtual a partir de diferentes perspectivas expertas.

La consulta anónima y por rondas permitió comparar alternativas, identificar riesgos, evitar decisiones basadas en una única opinión y alcanzar un consenso fundamentado.

Como resultado, se seleccionó una arquitectura de monolito modular en capas, con API segura, base de datos relacional transaccional, módulos desacoplados y componentes asíncronos para tareas no críticas.

Esta alternativa ofrece un equilibrio adecuado entre seguridad, confiabilidad, escalabilidad, costo y mantenibilidad para el desarrollo inicial de BilleteraSegura. Además, deja preparado al sistema para evolucionar hacia arquitecturas más distribuidas solo cuando las necesidades reales del producto lo justifiquen.

---

## Bibliografía utilizada

- Material de clase: **Método Delphi**.
- Material de apoyo: **Delphi_ES-1**.
- Informe de referencia: **Informe de resultados del Método Delphi**.
