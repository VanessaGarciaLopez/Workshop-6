- [Modelo Iot Básico](#modelo-iot-básico)
    - [Sensor](#sensor)
    - [Sistema Embebido](sistema-embebido)
          - [Hardware](#hardware)
          - [Software](#software)
    - [Conectividad](#conectividad)
    - [Análisis de Datos](#análisis-de-datos)
- [Simulación](#simulación)

# Modelo IoT Básico

El modelo planteado para este taller esta compuesto por 4 componentes, estos son:

## Sensor

El sensor utilizado fue el bmp280, este es un sensor de presión, temperatura y humedad.

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/bme280.jpg">
</p>

## Sistema Embebido

### Hardware

Se utilizó una raspberry pi conectada a un led y un sensor bmp280, ademas de esto se utilizó una protoboard para realizar un prototipado rápido que incluyera todos los elementos necesarios para el funcionamiento del sistema IoT.

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/raspberrypi3.jpg">
</p>

### Software

En el aspecto del software se utilizo node.js ya que ofrece un motor de ejecución robusto a pesar de estar escrito en un lenjuage de alto nivel como lo es javascript.

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/node.png">
</p>

## Conectividad

Para la conectividad se utilizo el IoT hub provisto por Azure, este permite crear una gran cantidad de dispositivos utilizando una interfaz muy simple y amigable la cual permite realizar estas conexiones de una forma rápida y efectiva utilizando los strings de conexión que son proveidos por la misma plataforma, una vez obtenido este string se procede a introducirlo en el codigo node.js que se ejecutara en la raspberry pi 3, en el cual solamente reemplazamos el string en el sitio donde deberia a ir y la conexión procede de una forma exitosa, esta conexión fue realizada mediante HTTP.

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/stringconexion.png">
</p>

## Análisis de Datos



# Simulación

La simulación se realizó en el "Raspberry Pi Azure Web Service", el cual nos permite prototipar de manera rápida e intuitiva utilizando protoboards, sensores y la Raspberry Pi 3, este fue el resultado de la simulación:

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/Prototipo.png">
</p>

En este caso el LED se enciende cada vez que la raspberry pi 3 envia con éxito un mensaje al IoT hub de azure, aquí podemos ver el código que permite realizar esta interacción con el IoT hub.

<p align="center">
  <img src="https://github.com/SadPac/Workshop-6/blob/main/img/sendmessage.png">
</p>

A su vez, la acción de comunicación conel IoT hub se realiza cada vez que el sensor le envía a la Raspberry Pi 3 una alerta de cambio de temperatura, en esta imagen se puede observar el código que genera estas instrucciones.

<p align="center">
  <img src="https://raw.githubusercontent.com/SadPac/Workshop-6/main/img/getmessage.png">
</p>


