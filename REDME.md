# Practica ESP32 con DHT22
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT22.

## Introducción

### Descripción

La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH11```) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado [WOKWI](https://https://wokwi.com/).

### Algunas aplicaciones para un DHT22
-Control de ambiente en criaderos 
-conservacion de alimentos 
-control de calidad para ciertas materias primas para la industria

## Material Necesario

Para realizar esta practica necesitas lo siguiente

- [WOKWI](https://https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT11



## Instrucciones

### Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://https://wokwi.com/).


### Instrucciones de preparación de entorno 

1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"
#include <LiquidCrystal_I2C.h>

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}

```
2. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/DiegoJm10/PracticaDHT/blob/main/Libreria%20DHT.png?raw=true)

3. Hacer la conexion de **DHT11** con la **ESP32** como se muestra en la siguente imagen.

![](https://raw.githubusercontent.com/DavidVar95/PRACTICA_DHT22/d7ded6c3fb3b2ccd9c7335f171fab8f34c765848/Captura%20de%20pantalla%202023-06-09%2021.00.01.png)

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT11** 

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![](https://raw.githubusercontent.com/DavidVar95/PRACTICA_DHT22/ac0b6ee4e64be1531f036eaf31fbd70720ade159/Captura%20de%20pantalla%202023-06-09%2020.51.50.png)




## Evidencias

[Video de Youtube](https://https://wokwi.com/)


# Créditos

Desarrollado por Ing. Diego Jasso Miranda

- [GitHub](https://github.com/DiegoJm10)