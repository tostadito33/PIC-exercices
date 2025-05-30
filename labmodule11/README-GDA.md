# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación extiende la funcionalidad del Gateway Device Application (GDA) al integrar comunicación bidireccional con la nube a través del servicio Ubidots utilizando MQTT seguro con autenticación por token y certificados TLS. El sistema publica periódicamente datos de sensores (temperatura, humedad, presión, etc.) y métricas de rendimiento del sistema (CPU, RAM) desde el GDA hacia Ubidots. Además, permite recibir comandos de actuadores desde la nube, como la activación de un LED o un sistema HVAC, reenviándolos al CDA para su ejecución.
How does your implementation work?
La integración se realiza a través de la clase CloudClientConnector, que hereda la lógica de conexión y comunicación de MqttClientConnector, pero adaptada para el entorno de Ubidots. Al iniciar, la clase establece una conexión MQTT segura con el broker de Ubidots utilizando credenciales autenticadas por token y TLS. Los datos de sensores y de rendimiento son serializados en formato JSON y publicados en los temas correspondientes de Ubidots. Al mismo tiempo, se mantiene una suscripción a temas que notifican eventos de actuadores. Al recibir un mensaje, se transforma en un objeto ActuatorData, que es procesado por DeviceDataManager y reenviado al CDA por MQTT local, lo que permite la ejecución física del comando (como encender un LED o activar una alarma).
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P11


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
