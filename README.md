# Investigación APRS-LORA

El siguiente repositorio busca....

## APRS

asd

## LoRa

El protocolo LoRaWAN, acrónimo de "Long Range Wide Area Network", es utilizado en comunicaciones que centran su búsqueda en la baja potencia, manteniendo un largo alcance y el cual está diseñado específicamente para el Internet de las Cosas (IoT). Este protocolo utiliza tecnología de radio LoRa (Long Range), para de esta manera poder trasmitir datos de manera eficiente sobre grandes distancias, todo esto con un consumo mínimo de energía, es justamente por esto que este protocolo es ideal para aplicaciones que necesiten de monitoreo y/o control remoto de dispositivo en áreas extensas, donde resaltan aplicaciones en agricultura inteligente, ciudades inteligentes, gestión de activos y medición inteligente.

En general, esta tecnología ofrece muchas ventajas, como su gran cobertura, bajo consumo energético, capacidad de manejar cientos de dispositivos con un solo gateway y alta capacidad de penetrar obstáculos urbanos y naturales. A parte de esto, el protocolo LoRaWAN, presentan una solución escalables y rentable, por lo que resulta atractiva en una amplia gama de aplicaciones.

La estructura básica de un sistema que utiliza este protocolo se puede observar en la siguiente figura, donde desde un LoRa NetServer, se genera una conexión con los gateways que sean necesarios, esto mediante conexiones IP y proporcionan la conexión a todos los demás dispositivos que sean de interés. Estos últimos se comunicarán mediante LoRa.

<p align="center">
    <img src="https://github.com/user-attachments/assets/c153f200-9acd-4e5c-8f52-e609523408b4"/>
</p>

# Historia

La creación y la historia como tal del protocolo comienza con el trabajo pionero realizado por la empresa Semtech Corporation, la cual en su momento estaba buscando soluciones para cumplir con los desafíos que presentó la conectividad en el campo emergente del internet de las cosas. Como resultado de esta buscada desarrollan su tecnología de modulación de largo alcance el cual se conoce ahora como LoRa, que como se mencionó anteriormente, se destaca por su alcance y bajo consumo energético.

Posteriormente, en el 2015, sea funda la LoRa Alliance, la cual es una asociación sin ánimo de lucro que busca el desarrollo de esta tecnología y la adopción del protocolo como un estándar con lo que respecta a la conectividad para la IoT, por lo cual la alianza ha buscado empresas líderes en tecnología, proveedores de servicio, operadores de red y por su puesto, desarrolladores de soluciones IoT, con el objetivo de establecer este marco común para la implementación de esta tecnología.

El ecosistema presente en LoRaWAN ha experimentado un crecimiento exponencial, con una amplia cantidad de soluciones puestas en diferentes industrias gracias a la gran cantidad de dispositivos certificados, lo que ha generado una creciente demanda en aplicaciones inteligentes conectadas a áreas de agricultura, logística y ciudades inteligentes. Este protocolo a demostrado una tecnología robusta y escalables que continuamente está transformando la forma en como interactuamos con el mundo, puesto a que ha abierto nuevas posibilidades en una amplia gama de aplicaciones y conforme la IoT continúa expandiéndose, se espera que LoRaWAN juegue cada vez más un papel más importante en la creación de un futuro más inteligente y conectado.

# Capa Física

La tecnología de modulación LoRa presenta un componente clave con lo que respecta a la capa física del sistema. Este protocolo utiliza la técnica de modulación de espectro ensanchado, para de esta manera enviar señales de radio con un ancho de banda más amplio que el de la señal inicial. Esto genera una mayor robustez contra la interferencia y el ruido que pueda estar presente. 

En la capa física también se presentan los esquemas de modulación y codificación específicos para mejorar la eficiencia espectral y la sensibilidad de recepción presente. Dentro de los esquemas presentes, como lo puede ser el \textit{Chirp Spread Spectrum} (CSS), se busca optimizar la capacidad de la red para así poder detectar y decodificar señales débiles en presencia de ruido y atenuación, lo que logra mejorar la confiabilidad de las comunicaciones a larga distancia.

## Implementación

asd
