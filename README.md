# Monitoreo-Simple-Clima-Sensor-DHT11-API-OpenWeather
Estación de monitoreo simple de clima grupal con el sensor DHT11 y un servidor en Node-Red.

### Descripción
En este programa se hace uso del código del repositorio “Flow-7-Medicion-De-Temperatura-ESP32CAM-DHT11-MQTT” como el código del microcontrolador ESP32 CAM para el funcionamiento del sensor DHT11. A esto se le agrega parte de los nodos del repositorio “Flow-5-OpenWheather” para obtener la información mediante API y desplegarla con nodos dashboard en Node-Red.

# Material
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
- Una cuenta en OpenWeather 

### Guías
Para configurar correctamente la IDE de Arduino para trabajar con el ESP32CAM, puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=850

Para configurar correctamente tu broker mosquitto puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=818

Para configurar correctamente NodeRed puedes consultar el siguiente enlace.

https://edu.codigoiot.com/course/view.php?id=817

Puedes obtener la biblioteca PubSubClient desde el siguiente enlace.

https://github.com/knolleary/pubsubclient

El microcontrolador publica en el tema `codigoIoT/ejemplo/mqtt` y lee en el tema `codigoIoT/ejemplo/mqtt`

El flow de NodeRed lee los datos del sensor en el tema `codigoIoT/ejemplo/mqtt` en localhost y los publica en el tema `codigoIoT/g7/mosquitto/sensores`. Para transmitir los datos del API el flow plubica en el tema `codigoIoT/g7/mosquitto/API` por lo que deberás configurar los nodos MQTT para conectarse a estos temas y al broker de tu elección.

## Funcionamiento
Para observar el funcionamiento de este proyecto deberás realizar lo siguiente.

### ESP32 CAM
1. Modificar el archivo ESP32ACM-DHT11-MQTT.ino con los el SSID y contraseña de tu red WiFi.
2. Carga el programa ESP32ACM-DHT11-MQTT.ino en el ESP32CAM.
3. Conectar el microcontrolador a la corriente eléctrica.

### Node-Red
1. Carga el flow Node-Red-Monitoreo-Simple-API-Sensor en NodeRed.
2. Modificar la latitud y longitud de las llamadas API para que correspondan con tu posición geográfica.
3. Modificar el appid de las llamadas por el de tu cuenta.
4. Modificar la IP a el Broker que usaras.
5. Comprueba que el broker publico  MQTT esté funcionando.
6. Visita el dashboard de NodeRed

![](https://github.com/EduCabreraMendoza/Monitoreo-Simple-Clima-Sensor-DHT11-API-OpenWeather/blob/main/Funcionamiento.jpeg)

Creado el 16-ago-2022 por [Eduardo Cabrera](https://github.com/EduCabreraMendoza)