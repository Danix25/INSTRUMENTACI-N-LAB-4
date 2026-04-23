# Diseño y construcción de una incubadora neonatal a escala

Samuel Joel Peña Rojas

Paula Vanessa Vera Caro

Daniel Leonardo López Castillo

## PARTE A

### Incubadora neonatal

Las incubadores neonatales se definen como dispositivos que proporcionan soporte térmico a los bebés, controlando a su vez los niveles de oxígeno y humedad relativa, con el objetivo de crear un entorno seguro para los recien nacidos. En este equipo se incorporan microprocesadores para la gestión precisa de estos parámetros críticos y requieren mantenimiento regular para garantizar su seguridad y funcionamiento.

<div align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/bb638f9e-1878-45ec-ae0a-ea6f7b558ed1" />
</div>

Estos equipos poseen una serie de sistemas que tienen el objetivo principal de emular el ambiente del vientre materno para asegurar la superviviencia del neonato. Las partes principales de una incubadora son:

- **Sistema de calefacción:** Es el componente esencial de la incubadora neonatal. Su diseño hace que mantenga una temperatura constante y adecuada para simular el útero materno. En este sistema se emplean elementos calefactores y sensores de temperatura para garantizar que el neonato se mantenga en condiciones óptimas, previniendo hipotermia o un sobrecalentamiento.

- **Control de humedad:** Este sistema es crucial para el bienestar del recien nacido. Aquí se usan humificadores automáticos y sensores para mantener un nivel óptimo de humedad, con el principal objetivo de prevenir la deshidratación y generar un ambiente sano.

- **Sistema de oxigenoterapia:** Mantener una buena oxigenación en las incubadores es fundamental para garantizar la vida del neonato, sobre todo para aquellos que requieren de soporte respiratorio. En este sistema actuan componentes reguladores de flujo, concentradores de oxígeno y monitores que permiten ajustar y controlar la concentración de oxígeno administrada, asegurando que el bebé reciba la cantidad necesaria para su desarrollo.

- **Monitoreo de signos vitales:** Este sistema es imprescindible en el cuidado neonatal, ya que permite la evaluación continua del estado de salud del recién nacido. Aquí se incluyen dispositivos específicos para medir parámetros como la frecuencia cardíaca, la temperatura corporal y la saturación de oxígeno en sangre, primordial para una atención adecuada y oportuna.

- **Sistemas de seguridad:** Para garantizar la seguridad del neonato, la incubadora cuenta con alarmas sonoras y visuales para alertar cambios críticos, así como tambien un sistema de bloqueo para evitar manipulaciones no autorizadas y el uso de materiales no tóxicos para mantener un entorno saludable para el recién nacido.

<div align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/43f5dadd-2fb7-4256-ad31-eb5725884c9a" />
</div>

### Diseño del circuito de temperatura

Para lograr una temperatura adecuada en una incubadora noenatal hecha a escala, se diseño un circuito eléctrico a modo de sistema de control tipo ON/OFF de temperatura, que permita mantener la variable térmica dentro de un rango fisiológico esctricto, comprendido entre los 36° C y 37,5° C, garantizando la estabilidad del sistema frente a perturbaciones externas. Esto se hizo a partir de un microcontrolador ESP32 y un sensor de temperatura DHT22, implementando una lógica de control gestionando una etapa de potencia con relevadores para regular los ciclos de calefacción y ventilación.

<div align="center">
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/6d2667bc-d43c-461a-8c52-3cc52aa44f1e" />
</div>

### Diseño del circuito de peso

El monitoreo del peso del neonato es un indicador clínico fundamental para evaluar su desarrollo y estado de salud. Para cumplir con este requerimiento, se diseñó un sistema de pesaje centrado en una celda de carga de 5 kg, la cual detecta cambios mecánicos mediante galgas extensiométricas. Para garantizar la fiabilidad de la medida, se integró un módulo de acondicionamiento de señal HX711, cuya resolución de 24 bits permite transformar las variaciones de microvoltios en datos digitales de alta precisión procesables por el microcontrolador.

<div align="center">
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/4cc03b1c-3750-46ac-98ca-81ebd1f981f9" />
</div>

## Parte B

Para materializar el prototipo, se inició con el montaje estructural de la cabina de la incubadora, siendo el lugar para proteger al neonato. Aquí se tuvo como enfoque principal la integración de todos los sistemas previamente diseñados en un solo entorno funcional, asegurando que la estructura permita una distribución adecuada del calor y soporte para el sistema de pesaje. Además de esto, es importante evaluzar nuestro estudio con equipos comerciales para situar el desempeño y costos de este desarrollo frente a soluciones tecnológicas utilizadas actualmente en el sector.

### Montaje de la cubierta

en cuanto a la consturcción del entorno físico, se inició con el montaje de la cubierta protectora. Sabiendo que el diseño de este componente tiene el enfoque de garantizar la visibilidad hacia el interior para el seguimiento clínico, así como tambien su seguridad y protección, se usaron materialez que optimizaran la retención de calor. Para esto, se uso una caja plástica con medidas aproximadas de 35 cm x 22 cm x 24 cm. Este material fue seleccionado por su transparencia, lo cual asegura la visibilidad requerida constante del neonato. De igual manera, la ligereza y propiedades aislantes del polímero ayudan a reducir la disipación térmica, mientras que la tapa original se modifico para funcionar como base del mecanismo, permitiendo un acceso seguro al interior de la incubadora.

<div align="center">
<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/a9ed2bc9-0696-4994-bb4a-94d849920171" />
</div>



