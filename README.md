# Mediciones Biomédicas con BLYNK

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


## Introducción.

Este proyecto experimental sirve para poder comprender las señales ECG y visualizar mediante la plataforma IOT Blynk.

Guía de la idea principal.

![alt text](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/guia1.jpg)


## Componentes utilizados:

- AD8232
- Módulo WIFI ESP8266
- Plataforma Blynk
- Smartphone con Android.

## Librerias:

| Nombre | Link |
| ------ | ------ |
| Blynk | https://github.com/blynkkk/blynk-library |
| ESP8266 | https://github.com/esp8266/Arduino |



El AD8232 es un pequeño chip limpio que se utiliza para medir la actividad eléctrica del corazón. Esta actividad eléctrica se puede graficar como un ECG o un electrocardiograma. [La electrocardiografía](http://www.google.com/url?q=http%3A%2F%2Fen.wikipedia.org%2Fwiki%2FElectrocardiography&sa=D&sntz=1&usg=AFQjCNFkfQENaNwNmE8lPuLXEWowH2vmDw) se utiliza para ayudar a diagnosticar diversas afecciones cardíacas. [La hoja de datos se puede encontrar aquí.](https://www.google.com/url?q=https%3A%2F%2Fcdn.sparkfun.com%2Fdatasheets%2FSensors%2FBiometric%2FAD8232.pdf&sa=D&sntz=1&usg=AFQjCNHg88_nHpAuxrkuqW3gXtkZb-oQyA)

![alt text](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/senbio00405_0322222.jpg?raw=true)
**Vista superior del AD8232.**


Junto a este chip utilizamos el módulo ESP8266, que sirve para conectar nuestros dispositivos a la red WiFi y así interactuar vía IoT (Internet of Things, en español Internet de las cosas).

Para visualizar la señal ECG se utiliza la aplicación Blynk. Esta misma te da la posibilidad de conectar arduino a IoT y generar un interfaz para poder mirar la señal.

![Captura de pantalla del interfaz de Blynk.](https://lh4.googleusercontent.com/QfvGizzcpzJI4Cjlx4MXzsBZHv4XG4Rb0xaQ-FmtfiXJzoYgxZvOPCQVzQ7iCO5l0tvpg9aDlKMl9DNvvRueiHA6uPPp1fymYuZ3SjfzxhL-PRC7ywVn=w271)
**Captura de pantalla del interfaz de Blynk.**

![Captura de pantalla de un widget de Blynk para ver la señal ECG.](https://lh4.googleusercontent.com/247a-3uPervsP4PMa4Mt1SyWyghgEpH0C7oN1ZWWEDVB_6XFAxxNX9zn0f83ldkz17nr2rlHQ_ai49UFrhKK3IJxRr_EefdvdLWouhOAyWSJSBhB1w=w874)

**Captura de pantalla de un widget de Blynk para ver la señal ECG.**


## Conexión:

![Conexión.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/wemos%20d1%20+%20ad8232.png?raw=true)

![enter image description here](https://lh5.googleusercontent.com/8JK63Phv6ORxzhL06qOYG7Gl3topoBwBHRNrdk0lsqvA8spvTfl9THBynx-LxE7vyDLgIg53=w371)
**Conexión en protoboard de ESP8266 y AD8232.**

## Configuración de Blynk:

![enter image description here](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/WhatsApp%20Image%202018-11-25%20at%2020.56.27%20(1).jpeg?raw=true)
**Elección del widget SuperChart para visualizar la señal.**

![enter image description here](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/WhatsApp%20Image%202018-11-25%20at%2020.56.27.jpeg?raw=true)

**Configuración del widget.**


## Sketch:
Para poder enlazar el ESP8266 (D1 mini) se hace un sketch en el IDE de Arduino para que pueda mandar los datos a Blynk.
El mismo lo subí a este **repositorio.** 

## Resultados:

![Señal ECG obtenida por el módulo AD8232.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/WhatsApp%20Image%202018-11-28%20at%2011.50.31%20(4).jpeg?raw=true)
**Señal ECG obtenida por el módulo AD8232.**

## Preguntas frecuentes:
- ¿Por qué no se puede visualizar bien la onda?

 Un posible problema podría ser que los parches estén mal conectados, tienes que fijarte que tengan gel en la parte de adentro, ya que el mismo le da continuidad. Si no tiene gel, se le pude aplicar un poco de alcohol en gel sobre la parte a conectar y eso ayuda a darle continuidad al parche.
 Otro problema que suele suceder es que si lo estás alimentando desde una PC de escritorio puede ser le haga interferencia y le produzca corrientes parásitas provenientes de la red. La solución es usar una notebook o netbook utilizando la batería. También se recomienda estar acostado de forma horizontal. (Link adafruit)


Fecha de ultima actualización: 19/2/2019
