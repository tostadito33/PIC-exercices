# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Esta implementación permite monitorear el rendimiento de la aplicación GDA, gestionando la recopilación de métricas de CPU y memoria. SystemPerformanceManager coordina las tareas SystemCpuUtilTask y SystemMemUtilTask, que heredan de BaseSystemUtilTask.

How does your implementation work?
El sistema inicia y detiene el monitoreo a través de SystemPerformanceManager, optimizando recursos y asegurando modularidad. Su arquitectura facilita la expansión con nuevas métricas y mejoras en la programación de tareas.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/tostadito33/java-components/tree/P2


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemCpuUtilTaskTest
- ConfigUtilTest
- SystemMemUtilTaskTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SystemPerformanceManagerTest
- GatewayDeviceAppTest
- 

EOF.
