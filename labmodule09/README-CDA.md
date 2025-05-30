# Constrained Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación desarrolla un cliente CoAP que actúa como interfaz de comunicación entre el sistema embebido y el Gateway Device Application (GDA). Este cliente es capaz de interactuar con recursos CoAP remotos mediante los métodos GET, POST, PUT y DELETE, permitiendo tanto la lectura como la actualización de información de sensores y actuadores. Además, integra una funcionalidad de observación de recursos, con la cual puede recibir notificaciones automáticas cuando los datos de un sensor cambian en el servidor.

How does your implementation work?
El cliente está construido utilizando la librería CoAPthon, y se encapsula en la clase CoapClientConnector. Esta clase gestiona el envío de mensajes CoAP construyendo rutas completas hacia los recursos definidos por el GDA. Al enviar peticiones, el cliente maneja las respuestas mediante funciones de callback que permiten procesar los datos recibidos e integrarlos en el flujo del sistema. Para la observación de recursos, se implementa un método que establece una suscripción persistente, actualizando el estado interno del cliente al recibir nuevos valores. El comportamiento fue verificado mediante pruebas locales, incluyendo la observación de recursos de temperatura y humedad, con validación en Wireshark.
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P9



### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest.py

- SystemCpuUtilTaskTest.py

- SystemMemUtilTaskTest.py

- ActuatorDataTest.py

- SensorDataTest.py

- SystemPerformanceDataTest.py

- HumiditySensorSimTaskTest.py

- PressureSensorSimTaskTest.py

- TemperatureSensorSimTaskTest.py

- HumidifierActuatorSimTaskTest.py

- HvacActuatorSimTaskTest.py

- CoapClientConnectorTest.py

- Todos los tests unitarios incluidos en part02


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py

- SystemPerformanceManagerTest.py

- SensorAdapterManagerTest.py

- ActuatorAdapterManagerTest.py

- DeviceDataManagerNoCommsTest.py

- SenseHatEmulatorQuickTest.py

- HumidityEmulatorTaskTest.py

- PressureEmulatorTaskTest.py

- TemperatureEmulatorTaskTest.py

- HumidifierEmulatorTaskTest.py

- HvacEmulatorTaskTest.py

- LedDisplayEmulatorTaskTest.py

- SensorEmulatorManagerTest.py

- ActuatorEmulatorManagerTest.py

- DataIntegrationTest.py

- MqttClientConnectorTest.py

- CoapClientConnectorTest.py


EOF.
