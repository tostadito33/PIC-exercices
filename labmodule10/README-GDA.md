# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Esta implementación permite que el Gateway Device Application (GDA) se comunique de manera segura con el Constrained Device Application (CDA) utilizando MQTT con autenticación y cifrado TLS. El GDA recibe datos de sensores (como humedad, temperatura y presión) publicados por el CDA, los analiza en tiempo real y, si detecta valores fuera de los rangos permitidos, genera comandos de actuador (por ejemplo, para activar un humidificador o un sistema HVAC). Además, el GDA también reenvía esta información a otras capas del sistema para su posterior análisis y procesamiento.


How does your implementation work?
El GDA utiliza la clase MqttAsyncClient para establecer una conexión MQTT asíncrona y segura con autenticación TLS utilizando certificados generados con OpenSSL. La clase MqttClientConnector gestiona la conexión, autenticación, suscripción a temas y recepción de mensajes. Los datos entrantes son procesados por DeviceDataManager, que convierte los mensajes JSON en objetos SensorData o ActuatorData, evalúa los valores, y si detecta condiciones críticas (como humedad por debajo del umbral), genera comandos de control que se envían de vuelta al CDA para su ejecución. Toda la lógica sigue un enfoque desacoplado para permitir su reutilización y testeo independiente.
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P10



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
