# Lab Module 12 - Semester Project - Final Write-up

NOTE: Be sure to implement all the Lab Module 12 requirements listed at Lab Module 12.


## Description

Este proyecto implementa un sistema IoT de detección de gases potencialmente peligrosos mediante sensores simulados conectados a un CDA (Connected Device Adapter), el cual envía los datos al GDA (Gateway Device Adapter) a través del protocolo MQTT sobre TLS. El GDA procesa esos datos, detecta situaciones críticas y envía comandos de actuación de vuelta al CDA o reenvía la información a la nube para su almacenamiento y análisis. El objetivo principal es desarrollar una solución sencilla, segura y funcional de monitoreo y control en entornos industriales o domésticos.


## What - The Problem 

Este proyecto busca abordar el riesgo asociado a la presencia de gases invisibles que pueden filtrarse en distintos entornos sin ser detectados de manera directa. Situaciones como esta pueden derivar en problemas graves si no se cuenta con un sistema que los identifique y actúe con rapidez. Por ejemplo, una fuga no detectada puede generar intoxicaciones, incendios, o incluso explosiones, dependiendo del tipo de gas.

La solución pretende funcionar como una herramienta preventiva que combine la recopilación automatizada de datos con la respuesta activa mediante actuadores. Con esto, se contribuye a aumentar la seguridad de instalaciones sin necesidad de supervisión humana constante, mejorando así la eficiencia del monitoreo ambiental.


## Why - Who Cares? 

En contextos como fábricas, almacenes o laboratorios, una fuga de gases puede representar un peligro real tanto para la infraestructura como para las personas. Por ello, desarrollar un sistema automatizado que detecte estas emisiones y reaccione apropiadamente puede ser una solución preventiva muy útil. Estos lugares muchas veces cuentan con equipos costosos o materiales sensibles, por lo que una respuesta rápida a niveles anormales de gases es fundamental.

Además, en un contexto académico o de formación profesional, este tipo de proyecto permite poner en práctica los fundamentos de sistemas conectados, protocolos de comunicación, seguridad en IoT, y simulación de sensores, lo cual es crucial para diseñar arquitecturas reales en el futuro.


## How - Expected Technical Approach

Logré desarrollar un emulador que simula lecturas provenientes de sensores de gas, temperatura y humedad, con valores realistas que representan concentraciones variables. Estos datos son enviados desde el CDA al GDA mediante MQTT sobre TLS, garantizando una conexión segura. El GDA procesa estos valores, detecta si se supera un umbral preestablecido, y en ese caso activa el actuador simulado (un ventilador).

El GDA también recoge información interna del sistema como uso de CPU, memoria y disco, promediados, y guarda estos datos junto con las últimas muestras del CDA en archivos planos. Toda esta información también se publica en la nube usando MQTT, donde puede ser visualizada o utilizada para activar eventos adicionales.

### System Diagram

[SENSOR CDA]
  |
  |  (MQTT over TLS)
  ↓
[GDA - Gateway]
  | \
  |  \__ Internal system stats (CPU, RAM, Disk)
  |
  |  (MQTT to cloud)
  ↓
[CLOUD SERVICE]




Write 1 to 2 paragraphs describing your design.



### What THREE (3) sensors and ONE (1) actuator did you use (add more if you wish)?

CDA Sensor 1: Presión

- CDA Sensor 2: Temperatura

- CDA Sensor 3: Humedad

- CDA Actuator 1: Ventilador



### What ONE (1) CDA protocol and TWO (2) GDA protocols did you implement (add more if you wish)?

- CDA to GDA Protocol: MQTT (con TLS)

- GDA to CDA Protocol: MQTT (comandos de actuador)

- GDA to Cloud Protocol: MQTT

- Cloud to GDA Protocol: MQTT (subscriptor de eventos de nube)


 
### What TWO (2) cloud services / capabilities did you use (add more if you wish)?

Cloud Service 1 (data ingress - all inputs): MQTT Broker en la nube para recolección de datos

Cloud Service 2 (data egress - all actuation events): MQTT Broker para envío de comandos a dispositivos a través del GDA



## Screen Shots Representing Cloud Services



### Screen Shots Representing Visualized Data

NOTE: Include (at least) TWO (2) screen shots - one showing at least 1 hour
of time-series data from the CDA, and one showing an event being triggered
that results in an actuation event sent to your GDA and then to your CDA.



EOF.
