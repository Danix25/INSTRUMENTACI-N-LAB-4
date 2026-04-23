# Diseño y construcción de una incubadora neonatal a escala

Samuel Joel Peña Rojas

Paula Vanessa Vera Caro

Daniel Leonardo López Castillo

## PARTE A

### Incubadora neonatal

Estos equipos incorporan diversos sistemas cuyo objetivo principal es emular las condiciones del entorno intrauterino, con el fin de garantizar la supervivencia y el adecuado desarrollo del neonato. A continuación, se describen los componentes principales de una incubadora neonatal:

-**Sistema de calefacción:** Constituye el componente esencial de la incubadora. Su función es mantener una temperatura estable y adecuada que simule las condiciones térmicas del útero materno. Para ello, se emplean elementos calefactores y sensores de temperatura que permiten regular el sistema, evitando tanto la hipotermia como el sobrecalentamiento del neonato.

-**Control de humedad:** Este sistema es fundamental para el bienestar del recién nacido. Utiliza humidificadores automáticos y sensores que permiten mantener niveles óptimos de humedad relativa, con el propósito de prevenir la deshidratación y favorecer un entorno fisiológicamente adecuado.

-**Sistema de oxigenoterapia:** La adecuada oxigenación es crítica en el cuidado neonatal, especialmente en pacientes que requieren soporte respiratorio. Este sistema integra reguladores de flujo, concentradores de oxígeno y dispositivos de monitoreo que permiten ajustar y controlar la concentración de oxígeno administrada, garantizando un suministro adecuado para el desarrollo del neonato.

-**Monitoreo de signos vitales:** Este sistema permite la evaluación continua del estado fisiológico del recién nacido. Incluye dispositivos destinados a la medición de parámetros como la frecuencia cardíaca, la temperatura corporal y la saturación de oxígeno en sangre, lo cual resulta esencial para una atención oportuna y adecuada.

-**Sistemas de seguridad:** Con el fin de garantizar la integridad del neonato, la incubadora dispone de mecanismos de seguridad que incluyen alarmas sonoras y visuales ante condiciones críticas, sistemas de bloqueo para prevenir manipulaciones no autorizadas y el uso de materiales biocompatibles, asegurando un entorno seguro y controlado.


<div align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/43f5dadd-2fb7-4256-ad31-eb5725884c9a" />
</div>

### Diseño del circuito de temperatura

Para garantizar una temperatura adecuada en una incubadora neonatal a escala, se diseñó un circuito eléctrico basado en un sistema de control tipo ON/OFF, orientado a mantener la variable térmica dentro de un rango fisiológico estricto, comprendido entre 36 °C y 37,5 °C, asegurando la estabilidad del sistema frente a posibles perturbaciones externas.

Este sistema fue implementado mediante el uso de un microcontrolador ESP32 y un sensor de temperatura DHT22, incorporando una lógica de control encargada de gestionar una etapa de potencia mediante relevadores, con el fin de regular los ciclos de calefacción y ventilación.


<div align="center">
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/6d2667bc-d43c-461a-8c52-3cc52aa44f1e" />
</div>

### Diseño del circuito de peso

El monitoreo del peso del neonato constituye un indicador clínico fundamental para la evaluación de su desarrollo y estado de salud. Para satisfacer este requerimiento, se diseñó un sistema de pesaje basado en una celda de carga de 5 kg, la cual permite detectar variaciones mecánicas mediante el uso de galgas extensiométricas.

Con el fin de garantizar la fiabilidad de la medición, se incorporó un módulo de acondicionamiento de señal HX711, cuya resolución de 24 bits permite convertir las variaciones de microvoltios en datos digitales de alta precisión, los cuales pueden ser procesados adecuadamente por el microcontrolador.


<div align="center">
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/4cc03b1c-3750-46ac-98ca-81ebd1f981f9" />
</div>

## Parte B

Para la materialización del prototipo, se inició con el montaje estructural de la cabina de la incubadora, concebida como el entorno destinado a la protección del neonato. En esta etapa, el enfoque principal estuvo orientado a la integración de todos los sistemas previamente diseñados en una única plataforma funcional, garantizando que la estructura permitiera una adecuada distribución térmica, así como el soporte mecánico necesario para el sistema de pesaje.

Adicionalmente, resulta fundamental contrastar el desarrollo propuesto con equipos comerciales, con el propósito de evaluar su desempeño y costos en relación con las soluciones tecnológicas actualmente empleadas en el sector.


### Montaje de la cubierta

En cuanto a la construcción del entorno físico, se inició con el montaje de la cubierta protectora. El diseño de este componente se orientó a garantizar la visibilidad hacia el interior para el seguimiento clínico, así como la seguridad y protección del neonato, empleando materiales que favorecieran la retención térmica.

Para este propósito, se utilizó una caja plástica con dimensiones aproximadas de 35 cm × 22 cm × 24 cm. Este material fue seleccionado por su transparencia, lo que permite una visualización continua del neonato. Asimismo, la ligereza y las propiedades aislantes del polímero contribuyen a reducir la disipación de calor. Adicionalmente, la tapa original fue modificada para funcionar como base estructural del sistema, facilitando un acceso seguro al interior de la incubadora.


<div align="center">
<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/a9ed2bc9-0696-4994-bb4a-94d849920171" />
</div>

### Montaje sistema de calefacción

Para la regulación del clima interno, se implementó un sistema de transferencia de calor por convección, integrando el circuito de control desarrollado en la fase anterior. Este mecanismo emplea la acción conjunta de un elemento resistivo (bombillo) como fuente de generación térmica y un ventilador de 12 V encargado de distribuir el flujo de aire de manera uniforme, con el objetivo de mantener la temperatura dentro de un rango estable entre 36 °C y 37,5 °C.

Con el fin de supervisar la variable térmica, se incorporó una interfaz basada en una pantalla OLED, la cual permite visualizar en tiempo real la temperatura interna de la incubadora. Adicionalmente, se implementaron dos indicadores luminosos (LED) para informar el estado del sistema: un LED rojo que señala condiciones fuera del rango óptimo y un LED azul que indica que la temperatura se encuentra dentro de los valores establecidos.

<div align="center">
<img width="464" height="441" alt="image" src="https://github.com/user-attachments/assets/259c4ae3-d46d-45a8-a330-8e17b29f237c" />
</div>


### Montaje sistema de pesaje

Para la medición del peso del neonato, se integró una celda de carga acoplada a la estructura de la base, con el fin de estimar el peso del recién nacido de manera no invasiva. Este valor se visualiza en tiempo real a través de la pantalla OLED previamente implementada.

Lo anterior permite obtener lecturas digitales precisas del estado del neonato, facilitando el seguimiento continuo de su crecimiento y desarrollo.


# REFERENCIAS

- [1] ScienceDirect, "Neonatal Incubator - an overview," ScienceDirect Topics, 2024. [En línea]. Disponible: https://www.sciencedirect.com/topics/nursing-and-health-professions/neonatal-incubator. [Accedido: 23-abr-2026].

- [2] J. Villalobos, "Partes de una incubadora neonatal," Prezi, 2018. [En línea]. Disponible: https://prezi.com/p/l6cj35j2nfv6/partes-de-una-incubadora-neonatal/. [Accedido: 23-abr-2026].




