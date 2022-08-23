# Monitoreo-Simple-Clima-Sensor-DHT11-API-OpenWeather
Estacion de monitoreo simple de clima grupal con el sensor DHT11 y un servidor en Node-Red.

### Descripción
En este programa se hace uso del código del repositorio “Flow-7-Medicion-De-Temperatura-ESP32CAM-DHT11-MQTT” como el código del microcontrolador ESP32 CAM para el funcionamiento del sensor DHT11. A esto se le agrega parte de los nodos del repositorio “Flow-5-OpenWheather” para obtener la información mediante API y desplegarla con nodos dashboard en Node-Red.

# Requisitos
Para que el código de este repositorio funcione, es necesario contar con lo siguiente:
 
- ESP32CAM
- IP Broker publico
- Programador FTDI con su cable
- Sensor DHT11
- Ubuntu 20.04
- IDE de Arduino 1.8 o superior
- Biblioteca PubSubClient para Arduino IDE
- Biblioteca WiFi para Arduino IDE
- Biblioiteca DHT de AdaFruit para Arduino IDE
- Broker Mosquitto funcionando de forma local en el puerto 1883
- NodeRed corriendo de forma local en el puerto 1880
- Nodos Dashboard para NodeRed

### Funcionamiento
Para observar el funcionamiento de este proyecto deberás realizar lo siguiente.

1. Carga el flow Node-Red-Monitoreo-Simple-API-Sensor en NodeRed.
2. Comprueba que el broker plublico MQTT esté funcionando.
3. Carga el programa ESP32ACM-DHT11-MQTT.ino en el ESP32CAM.
4. Visita el dashboard de NodeRed

![](https://github.com/EduCabreraMendoza/Monitoreo-Simple-Clima-Sensor-DHT11-API-OpenWeather/blob/main/Funcionamiento.jpeg)

Creado el 16-ago-2022 por [Eduardo Cabrera](https://github.com/EduCabreraMendoza)