# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
La implementación permite monitorear el rendimiento del sistema en una aplicación CDA, gestionando la recopilación de métricas de CPU y memoria. Para ello, se crea el módulo SystemPerformanceManager, que inicia y detiene las tareas de monitoreo, y la clase base BaseSystemUtilTask, de la cual heredan SystemCpuUtilTask y SystemMemUtilTask. Finalmente, se integran estas tareas en el administrador de rendimiento para una gestión centralizada.

How does your implementation work?
El sistema funciona activando SystemPerformanceManager, que programa y coordina las tareas de monitoreo. Cada tarea especializada hereda de la clase base, asegurando modularidad y reutilización del código. Al iniciar el monitoreo, el administrador ejecuta las tareas; al detenerlo, las finaliza, optimizando el uso de recursos y permitiendo futuras expansiones.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/python-components/tree/P2

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest
- 

EOF.
