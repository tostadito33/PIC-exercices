# Cloud Service Functions (Connected Devices)

## Lab Module 12 - Semester Project - CSF Components

Be sure to implement all the PIOT-CSF-* issues (requirements) listed.

### Description

What does your implementation do?
Mi implementación actúa como una aplicación GDA que simula la conexión segura entre un CDA local y la nube, utilizando MQTT sobre TLS como protocolo de comunicación. Recibe datos simulados desde sensores de temperatura y humedad, los procesa para detectar si se superan ciertos umbrales, y envía comandos de actuación cuando es necesario, como encender un ventilador. Además, recopila datos internos del sistema (CPU, memoria y disco) y almacena localmente una muestra representativa, a la vez que reenvía toda la información tanto del CDA como del propio GDA hacia la nube.

How does your implementation work?
La aplicación GDA conecta con el CDA mediante MQTT sobre TLS utilizando certificados generados con OpenSSL, asegurando una comunicación cifrada. Un hilo simula datos de sensores que el GDA interpreta y decide si necesita actuar. Si el valor del sensor supera un umbral, se genera un comando de actuador que se reenvía al CDA. Simultáneamente, se recopilan métricas internas del sistema (CPU, RAM, disco) y se almacenan junto con la última lectura del CDA en archivos planos. Todos los datos se publican en la nube usando MQTT, y el GDA también se suscribe a un tópico de comandos remotos desde la nube, ejecutando acciones locales en base a estos eventos.


### Code Documentation (only applies if you wrote CSF-specific code, otherwise, ignore)

#### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: 


#### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
- 
- 

#### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 

EOF.
