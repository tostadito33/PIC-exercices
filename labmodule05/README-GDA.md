# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación gestiona el flujo de datos entre los sensores y actuadores del CDA y el entorno externo, asegurando que la información recopilada se procese y se transmita correctamente a sistemas de almacenamiento o análisis. También permite la ejecución remota de comandos en los actuadores a través del GDA.

El módulo central, DeviceDataManager, facilita esta comunicación mediante protocolos como MQTT y CoAP, garantizando la correcta gestión de las conexiones. Además, la implementación supervisa el rendimiento del GDA, controlando métricas de CPU y memoria para optimizar su estabilidad y eficiencia.

How does your implementation work?

El funcionamiento del sistema se basa en un diseño modular que permite administrar la comunicación y el procesamiento de datos. Al iniciarse el GDA, DeviceDataManager establece las conexiones necesarias y empieza a recibir información de los sensores. Dependiendo de la configuración, estos datos pueden ser procesados, almacenados o reenviados a plataformas en la nube.

Cuando el GDA recibe un comando desde un sistema externo, lo interpreta y lo envía al CDA para su ejecución en los actuadores. Además, SystemPerformanceManager recopila datos sobre el rendimiento del sistema, asegurando su estabilidad. Al finalizar la ejecución, todos los módulos detienen sus procesos y liberan los recursos utilizados.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P5


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- SystemStateDataTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SystemPerformanceManagerTest
- DeviceDataManagerNoCommsTest
- DataIntegrationTest
- GatewayDeviceAppTest

EOF.
