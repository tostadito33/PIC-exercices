# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite la simulación y prueba de un sistema IoT sin necesidad de hardware físico, utilizando el emulador Sense HAT. Se conecta con módulos previos para emular sensores de temperatura, humedad y presión, así como actuadores como sistemas HVAC y humidificadores. Además, la matriz de LED del emulador se emplea para visualizar mensajes y estados del sistema, facilitando la validación y prueba del comportamiento del sistema en un entorno controlado.


How does your implementation work?

La implementación se basa en la interacción entre la CDA y el emulador Sense HAT. Se crean emuladores para sensores y actuadores, los cuales heredan de clases base y sobreescriben métodos para generar datos simulados. Los sensores proporcionan datos en tiempo real que son gestionados por el SensorAdapterManager, mientras que los actuadores, controlados por el ActuatorAdapterManager, responden a comandos para modificar el entorno simulado. La pantalla LED del emulador también se actualiza para reflejar las acciones realizadas.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: 


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
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
