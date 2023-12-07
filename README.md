## Adaptación y optimización del BITalino Revolution con Arduino Pro Mini para reducción de costos y propulsión de proyectos desde las aulas de clase

### Adaptation and optimization of the BITalino Revolution with Arduino Pro Mini for cost reduction and project propulsion from the classroom.

#
[![En Construcción](https://img.shields.io/badge/Estado-En%20Construcción-yellow)](#)

```
Bienvenidos al repositorio de Francisco Ruiz Garcia, estudiante de intercambio de la Universidad CES en convenio con la UPCH. Este repositorio corresponde al curso desarrollo profesional en bioingeniería 3, en donde se tratará de replicar una herramienta para la adquisición de señales biomédicas a bajo costo.
```

## Tabla de contenidos:
* [Resumen](#Resumen)
* [Materiales y métodos](#Materiales-y-métodos)
* [Principales hallazgos](#Principales-hallazgos)
* [Referencias](#Referencias)

## Resumen

El BITalino Revolution, desarrollado por Biosignals Plux, se presenta como una herramienta innovadora para capturar señales fisiológicas en la investigación médica y el desarrollo de tecnologías de salud. Este dispositivo de código abierto mide diversas señales biomédicas, desde la actividad muscular hasta la electrocardiografía, proporcionando a investigadores y desarrolladores una herramienta versátil para la creación de prototipos en el ámbito de la medicina y dispositivos portátiles de salud. El estudio aborda la reproducción del BITalino en un Arduino Pro Mini, eliminando la barrera económica con una reducción del costo del 85%. Este enfoque busca impulsar la producción de proyectos, superando limitaciones financieras y facilitando avances en la investigación médica y desarrollos tecnológicos.

## Materiales y métodos

| Materiales             | Imagen referencial                                              |
| ----------------- | ------------------------------------------------------------------ |
| <p align="justify"> *Arduino Pro Mini* es una placa de desarrollo de tamaño reducido que integra capacidades de conectividad inalámbrica.</p>| <img src="https://docs.arduino.cc/static/6ef0d448db73013667ac934fd00f5914/a207c/e000025_featured.jpg" alt= “logo1” height="200" width="400"> |
| <p align="justify"> *BITalino* es un kit de herramientas de prototipado rápido para proyectos de salud y bienestar personal. Incluye sensores inalámbricos y una plataforma de software para adquirir, procesar y visualizar datos biomédicos.</p>| <img src="http://cdn.shopify.com/s/files/1/0595/1068/5887/products/BITalino-Board.1.jpg?v=1646224819" alt= “logo1” height="200" width="400">|
| <p align="justify"> *USBASP* es un programador USB en-circuito(in-circuit) para los microcontroladores Atmel/Microchip AVR .</p>| <img src="https://europe1.discourse-cdn.com/arduino/original/4X/5/6/0/5608f59ee64985c581e9b36582e474aff15eda81.jpeg" alt= “logo1” height="200" width="400">|


La reproducción del BITalino Revolution en Arduino 
implica una serie de diversos procesos que incluyen el copiado 
del framework del Bitalino Revolution a una computadora, el 
pegado del mismo a Arduino Pro Mini, la configuración 
Bluetooth y el testeo. El Arduino Pro Mini utilizado tiene una 
alimentación de 3.3 V y su reloj funciona a 8 MHz.

 - Copiar framework BITalino a computador con sistema operativo Linux 
      ```
     avrdude -p m328p -c usbasp -P /dev/ttyACM0 -U flash:r:code_Bitalino.hex:i
      ```

- Pegar framework a Arduino Pro Mini
  ```
  avrdude -p m328p -c usbasp -P /dev/ttyACM0 -U flash:w:code_Bitalino.hex:i

    ```
## Principales hallazgos


| Imagen de referencias | Colocación electrodos en sujeto de prueba vista lateral |
|---|---|
| ![](/Documentation/Images/BITalino-Usbasp.jpg) | <p align="center"> Conexión BITalino-UsbASp </p>|
| ![](/Documentation/Images/Hex_BITalino.jpg) | <p align="center"> Archivo hexadecimal Arduino </p>|
| ![](/Documentation/Images/Arduino-Usbasp.jpg) | <p align="center"> Conexión Arduino-UsbASp </p>|
| ![](/Documentation/Images/Arduino-Bluetooth.jpg) | <p align="center"> Conexión Arduino-Bluetooth </p>|
| ![](/Documentation/Images/Señal-ArduinoRuido.jpg) | <p align="center"> Señal ruido </p>|



## Referencias

[1] “BITalino (r)evolution Plugged Kit BLE/BT,” PLUX 
Biosignals. Accessed: Dec. 06, 2023. [Online]. Available: 
https://www.pluxbiosignals.com/products/bitalinorevolution-plugged-kit-ble-bt

[2] S. Gao et al., “Use of Advanced Materials and Artificial 
Intelligence in Electromyography Signal Detection and 
Interpretation,” Advanced Intelligent Systems, vol. 4, no. 
10, p. 2200063, 2022, doi: 10.1002/aisy.202200063.

[3] S. Kaplan Berkaya, A. K. Uysal, E. Sora Gunal, S. Ergin, 
S. Gunal, and M. B. Gulmezoglu, “A survey on ECG 
analysis,” Biomedical Signal Processing and Control, 
vol. 43, pp. 216–235, May 2018, doi: 
10.1016/j.bspc.2018.03.003.

[4] “Tutorial Básico de Uso del Módulo Bluetooth HC-06 y 
HC-05,” Naylamp Mechatronics - Perú. Accessed: Dec. 
06, 2023. [Online]. Available: 
https://naylampmechatronics.com/blog/12_tutorialbasico-de-uso-del-modulo-bluetooth-hc-06-y-hc-05.html