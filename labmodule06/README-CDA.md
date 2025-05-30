# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Esta implementación introduce un sistema de control por umbral para dispositivos IoT que simula un sensor de temperatura y activa un ventilador virtual cuando se supera un valor límite. El propósito principal es demostrar un flujo básico de captura, análisis y reacción ante datos sensorizados, integrando componentes simulados para pruebas sin necesidad de hardware físico.

How does your implementation work?
El sistema funciona generando valores de temperatura simulados mediante un generador aleatorio, que son leídos periódicamente por el sistema. Cuando se detecta que el valor supera un umbral definido (por ejemplo, 30°C), se activa un actuador virtual representado por un mensaje de consola o log que indica que el ventilador ha sido encendido. El diseño sigue una arquitectura modular con clases separadas para el sensor, el actuador y la lógica de control. Se implementaron pruebas unitarias para cada componente, así como pruebas de integración que aseguran el comportamiento esperado del sistema completo ante diferentes escenarios de entrada.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P6


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SensorSimulatorTest  
- ThresholdControllerTest  
- ActuatorSimulatorTest  
- ConfigUtilTest  
- DataUtilTest 


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SensorActuatorWorkflowTest  
- ThresholdDecisionFlowTest  
- DeviceDataManagerTest 
- 

EOF.
