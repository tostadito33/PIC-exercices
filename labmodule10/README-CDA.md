# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación permite al CDA comunicarse de forma segura con el GDA utilizando MQTT con cifrado TLS. Está diseñada para enviar datos de sensores, rendimiento del sistema y estado de actuadores, así como para recibir comandos remotos del GDA que controlan dispositivos como el humidificador. Además, se implementa lógica local que analiza los datos de temperatura para activar automáticamente el sistema HVAC cuando sea necesario, sin depender de una instrucción remota.

How does your implementation work?
La implementación utiliza la función tls_set de la librería Paho MQTT para establecer una conexión segura mediante certificados generados con OpenSSL. Al recibir datos desde el GDA, el cliente MQTT del CDA los entrega al DeviceDataManager, que los convierte en objetos ActuatorData. A partir de ahí, el ActuatorDataManager actualiza el estado del humidificador según las instrucciones. Paralelamente, se ha integrado lógica de procesamiento local que activa el sistema HVAC automáticamente si la temperatura supera un umbral configurado, lo cual mejora la autonomía del CDA.
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P10


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
![image](https://github.com/user-attachments/assets/8566070d-809a-4e8e-a9cc-737b0eb2c9dd)
![image](https://github.com/user-attachments/assets/e6e55b28-3769-4fbd-95f3-1d28aa797492)

