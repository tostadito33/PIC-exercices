# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación añade un sistema de gestión de comandos de actuadores vía CoAP. Se ha desarrollado un manejador de recursos específico que permite recibir, almacenar y consultar comandos de actuadores enviados desde clientes remotos. Esto permite a otros sistemas externos controlar el comportamiento de los actuadores de manera remota, segura y estructurada, respetando los requisitos del módulo PIOT-GDA. Los recursos CoAP definidos son dinámicos y permiten adaptarse al tipo de actuador registrado.

How does your implementation work?
El sistema se basa en un recurso CoAP llamado ActuatorCommandResourceHandler, el cual extiende la funcionalidad de los recursos definidos en CoapServerGateway. Este recurso permite manejar peticiones PUT para actualizar el estado del actuador y peticiones GET para consultar su último valor. Internamente, el valor recibido se almacena utilizando el modelo de datos ActuatorData, y se integra con DeviceDataManager para su procesamiento. El recurso es accesible desde clientes externos que soporten el protocolo CoAP, y se probó exitosamente usando herramientas como Copper (Firefox plugin) y Wireshark.
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P8


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest

- ActuatorDataTest

- SensorDataTest

- DataUtilTest

- SystemPerformanceDataTest

- SystemStateDataTest

- ActuatorCommandHandlerTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- GatewayDeviceAppTest

- DeviceDataManagerTest

- CoapServerGatewayTest

- GetActuatorCommandResourceHandlerTest

- UpdateResourceHandlerTest

- ActuatorCommandIntegrationTest


EOF.
