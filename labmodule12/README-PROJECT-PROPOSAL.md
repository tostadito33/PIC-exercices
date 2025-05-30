# Lab Module 12 - Semester Project Proposal

## Description

Este proyecto consiste en la simulación de un sistema IoT distribuido que permita detectar niveles anómalos de gases en un entorno determinado mediante sensores virtuales. El sistema incluirá un CDA (Connected Device Adapter) que genera y transmite datos, un GDA (Gateway Device Adapter) que recibe, procesa y reenvía esa información, y servicios en la nube que almacenan y visualizan los datos. También se implementará un actuador simulado (un ventilador), que podrá ser activado automáticamente si se detectan niveles peligrosos.

El objetivo es desarrollar una solución simple pero funcional de monitoreo ambiental remoto, utilizando protocolos seguros y componentes típicos de arquitecturas IoT modernas.


## What - The Problem 

El problema a resolver es la detección temprana y respuesta automática ante la presencia de gases peligrosos, que en muchos casos son inodoros e invisibles. Esta situación es especialmente crítica en espacios cerrados como laboratorios, almacenes o industrias, donde una fuga de gas puede tener consecuencias graves si no se detecta a tiempo.

La falta de monitoreo continuo y de respuesta automatizada puede llevar a incidentes evitables. Por eso, este proyecto busca simular un sistema inteligente que no solo recoja información de sensores, sino que también actúe en función de ella, aumentando así la seguridad del entorno.


## Why - Who Cares? 

Este tipo de solución es importante porque muchas instalaciones carecen de sistemas eficientes y asequibles para la detección de gases. Contar con una arquitectura basada en IoT que pueda monitorear y responder automáticamente reduce la necesidad de intervención humana y mejora la seguridad general.

Personalmente, este proyecto permite reforzar conocimientos clave en sistemas distribuidos, comunicación segura entre dispositivos, emulación de sensores/actuadores, y conectividad en la nube, todos ellos fundamentales para el desarrollo de soluciones reales en el mundo de la tecnología conectada.


## How - Expected Technical Approach

La solución propuesta está compuesta por tres componentes principales: el CDA, que simula sensores de presión, temperatura y humedad, así como un ventilador actuador; el GDA, que recibe los datos, los analiza y decide si debe activar el actuador o enviar los datos a la nube; y los servicios cloud, que almacenan los datos y permiten su visualización o uso posterior.

El protocolo de comunicación entre el CDA y el GDA será MQTT sobre TLS, tanto para el envío de datos como para el envío de comandos al actuador. El GDA también usará MQTT para publicar información en la nube y suscribirse a eventos de control.****



## Results - Expected Outcomes 

Si el proyecto se ejecuta con éxito, se tendrá un sistema funcional que simula la interacción real de sensores y actuadores en una arquitectura IoT. El sistema será capaz de detectar niveles críticos de gases, actuar localmente activando un ventilador, y enviar los datos relevantes a un servicio cloud. Además, la información podrá ser utilizada para análisis histórico o visualización.

Esto también validará la correcta implementación de protocolos de comunicación seguros (MQTT sobre TLS), pruebas unitarias automatizadas, y gestión básica de datos en archivos planos. El proyecto será una base sólida y ampliable para futuras prácticas o implementaciones reales.


EOF.
