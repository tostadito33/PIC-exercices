# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación simula el funcionamiento de sensores y actuadores en un entorno IoT a través de la aplicación ConstrainedDeviceApp. Se han desarrollado estructuras de datos para representar sensores, actuadores y métricas de rendimiento del sistema, utilizando la clase base BaseIotData. A partir de ella, se derivan SensorData, ActuatorData y SystemPerformanceData, permitiendo una gestión organizada de la información.

Los sensores implementados incluyen humedad, temperatura y presión, mientras que los actuadores simulan el control de dispositivos como un humidificador y un sistema HVAC (Heating, Ventilation, and Air Conditioning). Los sensores generan telemetría en tiempo real, y los actuadores responden a comandos según las condiciones del entorno. Además, se han desarrollado gestores como SensorAdapterManager y ActuatorAdapterManager para centralizar la administración de los dispositivos y coordinar sus interacciones.


How does your implementation work?

La implementación sigue una estructura modular y jerárquica para garantizar un funcionamiento organizado. Se inicia con la creación de BaseIotData, que proporciona los atributos fundamentales para representar datos en dispositivos IoT. Luego, se derivan SensorData, ActuatorData y SystemPerformanceData, cada una con propiedades específicas.

Para la simulación de sensores, se implementa BaseSensorSimTask, que genera valores de telemetría de manera aleatoria o a partir de un conjunto de datos predefinido. De esta clase derivan HumiditySensorSimTask, PressureSensorSimTask y TemperatureSensorSimTask, cada una especializada en la captura de una métrica específica.

Los actuadores siguen un enfoque similar con BaseActuatorSimTask, que gestiona comandos de activación y desactivación. De esta derivan HumidifierActuatorSimTask y HvacActuatorSimTask, que permiten simular la respuesta de dispositivos físicos.

A nivel de gestión, SensorAdapterManager y ActuatorAdapterManager controlan la ejecución y monitoreo de sensores y actuadores, asegurando que los datos se procesen correctamente. Finalmente, DeviceDataManager actúa como un coordinador global, integrando sensores, actuadores y métricas de rendimiento del sistema.

El flujo final se cierra en ConstrainedDeviceApp, donde se instancia DeviceDataManager y se orquesta toda la ejecución del sistema. Esta estructura permite que los sensores recopilen datos, los actuadores respondan a condiciones específicas y la información fluya de manera eficiente en el sistema IoT simulado.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P3

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- HumiditySensorSimTaskTest
- PressureSensorSimTaskTest
- TemperatureSensorSimTaskTest
- HumidifierActuatorSimTaskTest
- HvacActuatorSimTaskTest
- BaseIotDataTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SensorAdapterManagerTest
- ActuatorAdapterManagerTest
- DeviceDataManagerNoCommsTest
- ConstrainedDeviceAppTest

EOF.
