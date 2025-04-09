# Investigación APRS-LORA - Grupo #2

El siguiente repositorio busca....

## APRS
<div align="justify">
El Automatic Packet Reporting System (APRS) es un sistema de comunicación digital utilizado en el ámbito de la radioafición que permite el intercambio de información en tiempo real, como ubicaciones GPS, datos meteorológicos, mensajes cortos o alertas de emergencia. Desarrollado en la década de 1990, combina tecnologías de radio packet y protocolos digitales para crear una red descentralizada y autónoma.
</div>

![image](https://github.com/user-attachments/assets/def326da-4361-4833-ac40-5fe74ba7b320)


# Historia
<div align="justify">
APRS nace en 1992 de la mente de Bob Bruninga (WB4APR), el cual era un ingeniero y radioaficionado que buscaba superar las limitaciones de las redes de packet radio de los años 80, ya que estas solo permitían mensajes de texto simples. Inspirado por sistemas militares como el PLRS, decidió adaptar el protocolo AX.25 para incluir datos geográficos, transformándolo en una herramienta para compartir ubicaciones en tiempo real.  Este esfuerzo se basó en su proyecto anterior, APLS, que había desarrollado en 1984 para rastrear vehículos en la Academia Naval, con el tiempo, APRS se convirtió en un sistema abierto y accesible para todos los radioaficionados.

Uno de los tantos momentos clave en la historia de APRS fue durante el Huracán Andrew en 1992, en ese entonces varios radioaficionados en Florida utilizaron el sistema para mapear las áreas afectadas y coordinar la ayuda, demostrando así su gran utilidad en situaciones de emergencia. A medida que avanzaba la tecnología, en los años 2000, APRS se benefició de la integración con GPS y la conexión a internet a través de servidores como APRS-IS, esto permitió que incluso aquellos sin equipos de radio pudieran acceder a la información en línea, lo cuál contribuyó a la utilización de APRS, además, se embarcó en proyectos innovadores, como la retransmisión de datos desde la Estación Espacial Internacional (ISS) y el seguimiento de globos estratosféricos.
</div>
# Capa Física

APRS emplea principalmente la modulación AFSK (Audio Frequency-Shift Keying) en FM, utilizando el estándar Bell 202 que opera a 1,200 baudios con tonos de 1,200 Hz y 2,200 Hz. Esta elección permite la compatibilidad con equipos analógicos más antiguos y radios portátiles de bajo costo, como los modelos de Baofengk, para las transmisiones más rápidas se utiliza FSK a 9,600 baudios, conforme a la norma G3RUH, que es común en enlaces UHF o en satélites como la ISS, que funciona como un digipeater.

El hardware esencial para APRS incluye varios componentes clave como el TNC (Terminal Node Controller) que es responsable de convertir señales digitales en tonos audibles, también se utilizan módems de tarjeta de sonido, en donde software como Dire Wolf emula un TNC utilizando la tarjeta de sonido de una computadora. Existen radios inteligentes, como el Kenwood TH-D74, que integran un GPS y un TNC interno.

# Ancho de Banda

El ancho de banda en APRS va de la mano con su técnica de modulación principal: AFSK (Audio Frequency-Shift Keying) como se mencionó anteriormente, en este esquema se ocupa un ancho de banda aproximado de 3-5 kHz, aunque el espacio asignado suele ser de 12.5 kHz o 25 kHz en canales VHF/UHF dependiendo de las regulaciones locales. Esta configuración equilibra la velocidad de transmisión con la necesidad de minimizar interferencias, permitiendo así que múltiples estaciones compartan la misma frecuencia sin solapamientos críticos, siempre que respeten protocolos de temporización y prioridad.

La gestión del ancho de banda en APRS es de suma importancia debido a la naturaleza descentralizada y pública de la red, aunque el sistema está diseñado para ser eficiente, el uso excesivo o configuraciones incorrectas, tales como tasas de transmisión muy altas, pueden saturar el canal, reduciendo  así la efectividad global. En bandas como 2 metros (144-148 MHz), donde APRS es común, la limitación de ancho de banda asegura que otros servicios, tales como voz o datos de alta velocidad coexistan sin problemas. Algunas implementaciones modernas, como APRS-IS (Internet), descargan tráfico a infraestructura en línea, aliviando la carga en el espectro radioeléctrico y optimizando el uso del ancho de banda analógico para fines prioritarios.

# Frecuencia

La frecuencia principal utilizada por el sistema APRS en la mayoría de los países es 144.390 MHz en la banda de 2 metros (VHF) principalmente en América del Norte y varias regiones, esta frecuencia ha sido estandarizada para facilitar la interoperabilidad entre radioaficionados a nivel global, lo que permite un monitoreo efectivo de los paquetes transmitidos. Un ejemplo de ello ocurre en Europa y otras regiones, en donde se pueden encontrar frecuencias como 144.800 MHz adaptándose a las regulaciones locales, si bien APRS puede operar en otras bandas, tales como 70 cm/UHF o incluso en HF, su uso es más común en VHF debido a su balance entre cobertura y ancho de banda. 

La elección de la frecuencia depende de factores tales como la disponibilidad del espectro, las normativas nacionales y el propósito de la comunicación. Por ejemplo, en entornos montañosos o rurales, la propagación en VHF es ideal para cobertura local, mientras que en HF (como 10 metros o 30 metros) se aprovecha para enlaces de larga distancia mediante reflexión ionosférica. Algunos satélites de radioaficionado, como la red CubeSat, también incluyen frecuencias APRS dedicadas (ej. 145.825 MHz). Es fundamental que los usuarios verifiquen las asignaciones de su región para evitar interferencias, ya que el uso incorrecto de frecuencias puede afectar servicios críticos o saturar canales compartidos. La coordinación con clubs locales y organizaciones como la IARU (International Amateur Radio Union) garantiza un uso responsable y eficiente del espectro.

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

# Ancho de Banda

Los valores de $BW$ usados comúnmente en LoRaWAN son los de $125 kHz, 250kHz$ y $500kHz$. Este valor afecta directamente la modulación y tiene algunas implicaciones:

**Distancia de trasmisión:** Al utilizar un $BW$ más estrecho, se puede aumentar la sensibilidad del receptor, por lo que se puede extender la distancia a la que se genera la comunicación. Por otra parte, esto puede generar una menor tolerancia a la interferencia.

**Tasa de datos:** Un $BW$ más amplio permite una tasa de datos más alta, por lo tanto se puede trasmitir más información en un mismo periodo de tiempo.

**Capacidad de penetración:** Si se utiliza un $BW$ más estrecho, se puede aumentar la capacidad de la señal de atravesar obstáculos, como lo pueden ser la vegetación o edificios.

# Frecuencia

Por otra parte, este protocolo permite trabajar en distintas bandas de frecuencia, como lo pueden ser $433 MHz$, $868 MHz$ y $915 MHz$, donde esto dependerá de la geografía y las regulaciones que se tengan en el país. La elección de la frecuencia a utilizar afecta de gran manera la cobertura, la capacidad de penetración y la interferencia que pueda estar presente en un área determinada, es por esto que se deben de tomar en cuenta estos últimos factores los cuales se pueden llamar externos, pero también se debe cuidar el uso del hardware a utilizar, puesto que, para lograr una comunicación exitosa, se necesita una buena elección tanto del dispositivo que maneja el módulo LoRa como de la antena encargada de enviar y/o recibir la información deseada.
Es también en esta capa donde se gestiona la potencia de transmisión y la sensibilidad de la recepción para de esta manera optimizar el rendimiento de la red, por lo que es necesario ajustar la potencia de salida en los dispositivos que transmiten y en las pasarelas para poder garantizar una comunicación de calidad y con el menor consumo de energía posible. 

Además de los aspectos mencionados anteriormente, la capa física presente en LoRaWAN también se influenciada por estándares y normativas relacionadas con regulaciones del espectro, la certificación de los equipos a utilizar y la interoperabilidad de dispositivos, la cual busca que las aplicaciones y los sistemas puedan intercambiar datos de manera segura y automática, dejando atrás los límites geográficos, políticos u organizativos.

## Implementación

asd
