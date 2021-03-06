# Mediciones Biomédicas con BLYNK

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


## Introducción.

Este proyecto experimental sirve para poder comprender las señales ECG y visualizar mediante la plataforma IOT Blynk.

Guía de la idea principal.

![alt text](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/guia.jpg)


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

![vista superior](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/senbio00405_0322222.jpg)

**Vista superior del AD8232.**


Junto a este chip utilizamos el módulo ESP8266, que sirve para conectar nuestros dispositivos a la red WiFi y así interactuar vía IoT (Internet of Things, en español Internet de las cosas).

Para visualizar la señal ECG se utiliza la aplicación Blynk. Esta misma te da la posibilidad de conectar arduino a IoT y generar un interfaz para poder mirar la señal.

![Captura](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen1.jpg)
**Captura de pantalla del interfaz de Blynk.**

![Captura de pantalla de un widget de Blynk para ver la señal ECG.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen2.jpg)

**Captura de pantalla de un widget de Blynk para ver la señal ECG.**


## Conexión:

![Conexión.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/diagrama-wemosd1-ad8232.jpg)

![enter image description here](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen7.jpg)
**Conexión en protoboard de ESP8266 y AD8232.**

## Configuración de Blynk:

![enter image description here](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen1.jpg)
**Elección del widget SuperChart para visualizar la señal.**

![configuracion](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen2.jpg)

**Configuración del widget.**


## Sketch:
Para poder enlazar el ESP8266 (D1 mini) se hace un sketch en el IDE de Arduino para que pueda mandar los datos a Blynk.
El mismo lo subí a este **repositorio.** 

## Resultados:

![Señal ECG obtenida por el módulo AD8232.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen4.jpg)

![Señal ECG obtenida por el módulo AD8232.](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/Imagen3.jpg)

**Señal ECG obtenida por el módulo AD8232.**

## Videos:


[![Watch the video](https://github.com/pablolezcano/Mediciones-Biom-dicas-con-la-plataforma-IOT-Blynk/blob/master/imagenes/reproductor-youtube-diseno-plano_23-2147837761~2.jpg)](https://drive.google.com/file/d/1QLu-7aLiRvvh0Hy2KowzTReqTFM5gfuV/view?usp=drivesdk)

## Preguntas frecuentes:
- ¿Por qué no se puede visualizar bien la onda?

 Un posible problema podría ser que los parches estén mal conectados, tienes que fijarte que tengan gel en la parte de adentro, ya que el mismo le da continuidad. Si no tiene gel, se le pude aplicar un poco de alcohol en gel sobre la parte a conectar y eso ayuda a darle continuidad al parche.
 Otro problema que suele suceder es que si lo estás alimentando desde una PC de escritorio puede ser le haga interferencia y le produzca corrientes parásitas provenientes de la red. La solución es usar una notebook o netbook utilizando la batería. También se recomienda estar acostado de forma horizontal. (Link adafruit)



