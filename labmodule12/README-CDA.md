# Constrained Device Application (Connected Devices)

## Lab Module 12 - Semester Project - CDA Components

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
La implementación desarrollada simula un sistema básico de IoT compuesto por un sensor de temperatura y un actuador que responde a los valores generados por el sensor. El sensor genera valores de temperatura simulados dentro de un rango definido, y el actuador toma decisiones para encender o apagar un ventilador basado en un umbral de temperatura configurado. Esta implementación permite demostrar el flujo típico de lectura de datos sensoriales, procesamiento de dichos datos y actuación sobre un dispositivo conectado, todo ello en un entorno simulado.

El sistema funciona generando telemetría de temperatura con el sensor emulado, que produce valores aleatorios dentro del rango predefinido. Estos datos son recibidos por el actuador emulado, que evalúa si la temperatura supera un umbral establecido (25 grados Celsius) para decidir si debe activar o desactivar el ventilador. La comunicación se realiza mediante objetos de datos que encapsulan valores y comandos, facilitando así la interacción entre componentes. Además, se han desarrollado pruebas unitarias para validar que el actuador responde correctamente en situaciones de temperatura alta o normal, asegurando la fiabilidad del comportamiento.
How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P12


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- TempSensorActuatorTest
- 
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 

EOF.
