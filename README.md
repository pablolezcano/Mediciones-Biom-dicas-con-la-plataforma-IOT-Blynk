# Mediciones Biomédicas con BLYNK

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


## Introducción.

Este proyecto experimental sirve para poder comprender las señales ECG y visualizar mediante la plataforma IOT Blynk.

Guía de la idea principal.

![alt text](https://i.ibb.co/SyHTMN8/guia.jpg)


## Componentes utilizados:

- AD8232
- Módulo WIFI ESP8266
- Plataforma Blynk
- Smartphone con Android o iOS.

## Librerias:

| Nombre | Link |
| ------ | ------ |
| Blynk | https://github.com/blynkkk/blynk-library |
| ESP8266 | https://github.com/esp8266/Arduino |



El AD8232 es un pequeño chip limpio que se utiliza para medir la actividad eléctrica del corazón. Esta actividad eléctrica se puede graficar como un ECG o un electrocardiograma. [La electrocardiografía](http://www.google.com/url?q=http%3A%2F%2Fen.wikipedia.org%2Fwiki%2FElectrocardiography&sa=D&sntz=1&usg=AFQjCNFkfQENaNwNmE8lPuLXEWowH2vmDw) se utiliza para ayudar a diagnosticar diversas afecciones cardíacas. [La hoja de datos se puede encontrar aquí.](https://www.google.com/url?q=https%3A%2F%2Fcdn.sparkfun.com%2Fdatasheets%2FSensors%2FBiometric%2FAD8232.pdf&sa=D&sntz=1&usg=AFQjCNHg88_nHpAuxrkuqW3gXtkZb-oQyA)

![alt text](https://lh3.googleusercontent.com/-4P8f28zRm-wsjHxSEAPNS7eP0Ba8V68EvsYifjYN7C4dbzWpafizacCefCAtQjp4nZCZ6F3=w371)
**Vista superior del AD8232.**

![alt text](https://lh4.googleusercontent.com/yutNu6VZSA2hBRm2IKkf-vmsVopUUKJzbAfvXZCnOUTvh8Ji3wqk_PBN9uLVN1HtD3gmWMhlmm1U-HNfWC5H6NzNCm0W_LIg_n38brV5hC0yLegLmPI=w271)
**Vista trasera del AD8232.**

Junto a este chip utilizamos el módulo ESP8266, que sirve para conectar nuestros dispositivos a la red WiFi y así interactuar vía IoT (Internet of Things, en español Internet de las cosas).

Para visualizar la señal ECG se utiliza la aplicación Blynk. Esta misma te da la posibilidad de conectar arduino a IoT y generar un interfaz para poder mirar la señal.

![Captura de pantalla del interfaz de Blynk.](https://lh4.googleusercontent.com/QfvGizzcpzJI4Cjlx4MXzsBZHv4XG4Rb0xaQ-FmtfiXJzoYgxZvOPCQVzQ7iCO5l0tvpg9aDlKMl9DNvvRueiHA6uPPp1fymYuZ3SjfzxhL-PRC7ywVn=w271)
**Captura de pantalla del interfaz de Blynk.**

![Captura de pantalla de un widget de Blynk para ver la señal ECG.](https://lh4.googleusercontent.com/247a-3uPervsP4PMa4Mt1SyWyghgEpH0C7oN1ZWWEDVB_6XFAxxNX9zn0f83ldkz17nr2rlHQ_ai49UFrhKK3IJxRr_EefdvdLWouhOAyWSJSBhB1w=w874)

**Captura de pantalla de un widget de Blynk para ver la señal ECG.**


## Conexión.

![Conexión.](https://lh6.googleusercontent.com/ZK69YQfNjN5SLeswwZd1nDeWO0n0JEMDyHFH02vPiYorCZ_EOO6jMOHn9FlRbGpFU1_ptxMBb998h9daEEU1dD6hMHb8eRJPD-5idG_b06tlhzqLAA=w572)

![enter image description here](https://lh5.googleusercontent.com/8JK63Phv6ORxzhL06qOYG7Gl3topoBwBHRNrdk0lsqvA8spvTfl9THBynx-LxE7vyDLgIg53=w371)
**Conexión en protoboard de ESP8266 y AD8232.**

## Configuración de Blynk.

![enter image description here](https://lh6.googleusercontent.com/3My3maXM_7AMXw2nQAKwER-6Y1KlSoKkZlLtKDK90eZWj8_1z2ah6uzZXItraKYE6utyCqw=w371)
**Elección del widget SuperChart para visualizar la señal.**

![enter image description here](https://lh5.googleusercontent.com/-YSrbkkdYkFQ2fMz7T-pcXZy9BRnFlFYxn7gGvude9T24MXke_lVzxMlj8bgDU---zQK1tLNhw=w371)

**Configuración del widget.**


## Sketch.
Para poder enlazar el ESP8266 (D1 mini) se hace un sketch en el IDE de Arduino para que pueda mandar los datos a Blynk.
El mismo lo subí a este **repositorio.** 

## Resultados.

![Señal ECG obtenida por el módulo AD8232.](https://lh4.googleusercontent.com/FabBnyfKNQ7B_kxzghTbYFDijIKXdWiFNflBjt8fMXaunV0UQTjv_awFM9-593JGe8tVfPQqfRvKfo3xwNkY9SK-Vw4zcoZ0cYyOpmI2T_d3S7EKhhg=w673)
**Señal ECG obtenida por el módulo AD8232.**




Fecha de ultima actualización: 13/2/2019
