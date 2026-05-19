# Ejercicio Nro: 13

## Enunciado
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. A continuación se detallan las etapas de desarrollo utilizando TDD:

Etapa 1: Especificación y prueba inicial
  1) Especifica los requisitos básicos del sistema y las funcionalidades clave, como la apertura de cuenta, depósito de fondos, retiro de fondos y transferencia de fondos.
  2) Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.
     
Etapa 2: Desarrollo de las funcionalidades básicas
  1) Implementa la funcionalidad para abrir una cuenta bancaria, asegurándote de que se cumplan los requisitos especificados. Ejecuta la prueba y verifica que pase correctamente.
  2) Implementa la funcionalidad para realizar depósitos en una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
  3) Implementa la funcionalidad para realizar retiros de una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
  4) Implementa la funcionalidad para transferir fondos entre cuentas bancarias. Ejecuta las pruebas y verifica que pasen correctamente.

Etapa 3: Pruebas adicionales y mejoras
  1) Escribe pruebas adicionales para cubrir casos de prueba específicos, como intentar retirar más dinero del disponible en una cuenta o transferir fondos a una cuenta inexistente.
  2) Ejecuta todas las pruebas y verifica que pasen correctamente.
  3) Refactoriza tu código si es necesario para mejorar su estructura, legibilidad y eficiencia.
  4) Ejecuta todas las pruebas nuevamente para asegurarte de que el código refactorizado no haya introducido errores.

Etapa 4: Cobertura completa de pruebas
  1) Asegúrate de que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas.
  2) Examina los casos límite y situaciones excepcionales para garantizar que el sistema se comporte correctamente en todos los escenarios.
  3) Ejecuta todas las pruebas y verifica que pasen correctamente.

Recuerda seguir el enfoque TDD, donde agregarás una prueba antes de implementar cada funcionalidad y verificarás que todas las pruebas pasen antes de pasar a la siguiente etapa. Esto te ayudará a desarrollar una aplicación confiable, mantenible y que cumpla con los requisitos establecidos.

## Resolución
# Etapa 1: Especificación y prueba inicial

1. Requisitos básicos del sistema

El sistema debe permitir:

  - Crear una cuenta bancaria.
  - Consultar el saldo inicial de la cuenta.
  - Realizar depósitos.
  - Realizar retiros.
  - Transferir fondos entre cuentas.
  - Validar que no se puedan hacer operaciones inválidas.

Como requisitos principales, una cuenta bancaria debe tener un identificador, un titular y un saldo. Al abrir una cuenta, el saldo inicial puede ser cero o un monto inicial definido.


2. Prueba inicial

La primera prueba debe verificar que el sistema pueda crear una cuenta bancaria correctamente y obtener su saldo inicial.

Prueba planteada:
Crear una cuenta bancaria nueva con saldo inicial igual a $0 y verificar que el saldo obtenido sea $0.

Resultado esperado:
La cuenta se crea correctamente y el saldo inicial coincide con el valor definido.


# Etapa 2: Desarrollo de funcionalidades básicas
3. Apertura de cuenta bancaria

Primero se plantea una prueba para verificar que una cuenta pueda abrirse con datos válidos.

Prueba:
Crear una cuenta con titular, número de cuenta y saldo inicial.

Resultado esperado:
El sistema debe registrar la cuenta y permitir consultar sus datos.

Implementación esperada:
Se define una estructura básica de cuenta bancaria con titular, número de cuenta y saldo.


4. Depósito de fondos

La siguiente funcionalidad es permitir depósitos.

Prueba:
Depositar $1000 en una cuenta con saldo inicial $0.

Resultado esperado:
El saldo final debe ser $1000.

También debería contemplarse que no se permitan depósitos con montos negativos o iguales a cero.


5. Retiro de fondos

Luego se plantea la funcionalidad de retiro.

Prueba:
Retirar $500 de una cuenta que tiene $1000.

Resultado esperado:
El saldo final debe ser $500.

Además, el sistema debe evitar retiros superiores al saldo disponible.


6. Transferencia entre cuentas

La aplicación debe permitir transferir fondos entre dos cuentas bancarias.

Prueba:
Transferir $300 desde una cuenta con saldo $1000 hacia otra cuenta con saldo $200.

Resultado esperado:
La cuenta origen debe quedar con $700 y la cuenta destino con $500.

También debe validarse que la cuenta destino exista y que la cuenta origen tenga saldo suficiente.

# Etapa 3: Pruebas adicionales y mejoras
7. Pruebas adicionales

Se agregan pruebas para cubrir casos particulares y situaciones de error:

  - Intentar retirar más dinero del disponible.
  - Intentar depositar un monto negativo.
  - Intentar transferir fondos a una cuenta inexistente.
  - Intentar transferir un monto mayor al saldo disponible.
  - Intentar abrir una cuenta sin titular.

Resultado esperado:
El sistema debe rechazar estas operaciones y mostrar un error o mensaje adecuado.


8. Ejecución de todas las pruebas

Una vez definidas las pruebas principales y adicionales, se ejecutan todas para verificar que el comportamiento del sistema sea correcto.

Resultado esperado:
Todas las pruebas deben pasar correctamente antes de continuar.


9. Refactorización del código

Si el código funciona pero puede mejorarse, se aplica refactorización.

Posibles mejoras:

  - Separar responsabilidades.
  - Mejorar nombres de métodos y variables.
  - Evitar duplicación de lógica.
  - Ordenar validaciones.
  - Mejorar la legibilidad del código.

El objetivo de la refactorización no es cambiar el comportamiento del sistema, sino mejorar su estructura interna.


10. Nueva ejecución de pruebas

Después de refactorizar, se vuelven a ejecutar todas las pruebas.

Resultado esperado:
Todas las pruebas deben seguir pasando correctamente, demostrando que los cambios internos no rompieron funcionalidades existentes.

# Etapa 4: Cobertura completa de pruebas
11. Funcionalidades cubiertas por pruebas automatizadas

Se verifica que todas las funcionalidades principales estén cubiertas por pruebas:

  - Apertura de cuenta.
  - Consulta de saldo.
  - Depósito.
  - Retiro.
  - Transferencia.
  - Validación de errores.

Esto permite asegurar que el sistema pueda mantenerse y modificarse con menor riesgo.


12. Casos límite y situaciones excepcionales

Se analizan casos extremos para comprobar que el sistema responda correctamente:

  - Saldo inicial negativo.
  - Depósito de monto cero.
  - Retiro de monto cero.
  - Transferencia a cuenta inexistente.
  - Transferencia desde cuenta sin saldo suficiente.
  - Cuenta sin titular.
  - Operaciones con valores inválidos.

Resultado esperado:
El sistema debe impedir operaciones incorrectas y conservar la integridad de los datos.

13. Ejecución final de pruebas

Finalmente se ejecuta el conjunto completo de pruebas automatizadas.

Resultado esperado:
Todas las pruebas deben pasar correctamente, confirmando que el sistema cumple con los requisitos definidos.


## Conclusión

Aplicar TDD en el desarrollo de una aplicación bancaria permite construir el sistema de forma ordenada, comenzando por las pruebas y luego implementando cada funcionalidad. Esto ayuda a detectar errores de manera temprana, mejorar la calidad del software y facilitar futuras modificaciones sin afectar el comportamiento esperado del sistema.
