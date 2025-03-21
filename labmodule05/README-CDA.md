# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación se encarga de recopilar datos de telemetría, como el rendimiento de la CPU y la memoria, y de convertir la información de sensores y actuadores a formato JSON y viceversa. En el CDA, los módulos SensorDataManager y ActuatorDataManager se ocupan de la adquisición y transformación de los datos, permitiendo que la información del hardware se estructure antes de ser enviada al GDA. Este enfoque garantiza que los datos de los sensores se transmitan correctamente y que los actuadores reciban instrucciones precisas.


How does your implementation work?

El funcionamiento de la implementación se basa en la organización de los datos mediante clases especializadas para sensores y actuadores. SensorDataManager obtiene información de los sensores, la formatea en JSON y la envía, mientras que ActuatorDataManager recibe comandos en formato JSON, los interpreta y ejecuta las acciones en los actuadores.

La comunicación entre CDA y GDA se lleva a cabo utilizando protocolos como MQTT o CoAP. Además, SystemPerformanceManager ha sido actualizado para recopilar información sobre la CPU y la memoria, y DataUtil permite la conversión de los datos de sensores y actuadores entre JSON y su formato original.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P5


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- DataUtilTest
- ConfigUtilTest
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SystemPerformanceManagerTest
- DataIntegrationTest
- ConstrainedDeviceAppTest
- DeviceDataManagerNoCommsTest

EOF.
