# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación incorpora un sistema de notificación por umbral para el GDA, permitiendo que se genere una alerta cuando los valores de sensores simulados (como temperatura o humedad) superan ciertos límites definidos en la configuración. Se ha desarrollado una nueva clase llamada ThresholdAlertManager, la cual evalúa los datos entrantes en tiempo real y dispara una alerta lógica en el sistema cuando se detecta una condición crítica. Esta funcionalidad está diseñada para ser extensible y configurable por el usuario.

How does your implementation work?
El componente ThresholdAlertManager se integra dentro del flujo de datos gestionado por DeviceDataManager. Cada vez que se recibe una nueva lectura de sensor, el sistema evalúa si alguno de los valores excede los límites permitidos. Si es así, se activa un manejador de alertas, que actualmente registra el evento y simula un envío a un sistema externo de respuesta (por consola o log). Este módulo está implementado de forma desacoplada para facilitar futuras integraciones, como notificaciones por email o conexión a una API externa. Se ha verificado su comportamiento con pruebas unitarias y escenarios de integración específicos.
### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P7


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest  
- SensorDataTest  
- ActuatorDataTest  
- SystemStateDataTest  
- ThresholdAlertManagerTest  
- DataUtilTest  

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- DeviceDataManagerTest  
- GatewayDeviceAppTest  
- ThresholdAlertIntegrationTest  
- DataIntegrationTest  

EOF.
