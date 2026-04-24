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
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/76e20320-f824-4a05-8220-3231b378b441" />
</div>

### Diseño del circuito de temperatura

Para garantizar una temperatura adecuada en una incubadora neonatal a escala, se diseñó un circuito eléctrico basado en un sistema de control tipo ON/OFF, orientado a mantener la variable térmica dentro de un rango fisiológico estricto, comprendido entre 36 °C y 37,5 °C, asegurando la estabilidad del sistema frente a posibles perturbaciones externas.

Este sistema fue implementado mediante el uso de un microcontrolador ESP32 y un sensor de temperatura DHT22, incorporando una lógica de control encargada de gestionar una etapa de potencia mediante relevadores, con el fin de regular los ciclos de calefacción y ventilación.


<div align="center">
<img width="600" height="400" alt="Diagrama de Conexion" src="https://github.com/user-attachments/assets/3bf43457-5eae-496f-8d9e-76f6a03ae5ed" />
</div>

### Diseño del circuito de peso

El monitoreo del peso del neonato constituye un indicador clínico fundamental para la evaluación de su desarrollo y estado de salud. Para satisfacer este requerimiento, se diseñó un sistema de pesaje basado en una celda de carga de 5 kg, la cual permite detectar variaciones mecánicas mediante el uso de galgas extensiométricas.

Con el fin de garantizar la fiabilidad de la medición, se incorporó un módulo de acondicionamiento de señal HX711, cuya resolución de 24 bits permite convertir las variaciones de microvoltios en datos digitales de alta precisión, los cuales pueden ser procesados adecuadamente por el microcontrolador.


<div align="center">
<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/4cc03b1c-3750-46ac-98ca-81ebd1f981f9" />
</div>

Posteriormente, la información obtenida sobre la masa del bebé y la temperatura de la incubadora se muestra en una pantalla OLED.

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

Para la regulación del clima interno, se implementó un sistema de control de temperatura basado en un elemento resistivo (bombillo) como fuente de generación de calor y un ventilador de 12 V como mecanismo de enfriamiento. El sistema opera de forma automática mediante un control por umbrales: el ventilador se activa cuando la temperatura supera los 37,5 °C para reducir el calor interno, y se desactiva cuando la temperatura desciende a 35,9 °C, momento en el cual el bombillo vuelve a encenderse para incrementar nuevamente la temperatura, manteniéndola dentro del rango establecido.

Con el fin de supervisar la variable térmica, se incorporó una interfaz basada en una pantalla OLED, la cual permite visualizar en tiempo real la temperatura interna de la incubadora. Adicionalmente, se implementaron dos indicadores luminosos (LED): un LED azul que se enciende cuando la temperatura se encuentra dentro del rango normal establecido (36 °C a 37,5 °C), y un LED rojo que indica condiciones fuera de dicho rango.

<div align="center">
<img width="464" height="441" alt="image" src="https://github.com/user-attachments/assets/259c4ae3-d46d-45a8-a330-8e17b29f237c" />
</div>

<p align="center">
  <img src="https://github.com/user-attachments/assets/604aabbd-80be-4148-9d67-b5702ab73d03" width="400" height="350">
  <img src="https://github.com/user-attachments/assets/ab0c1c44-29c5-4bf3-8c0a-142acee40a7e" width="400" height="350">
</p>


### Montaje sistema de pesaje

Para la medición del peso del neonato, se integró una celda de carga acoplada a la estructura de la base, con el fin de estimar el peso del recién nacido de manera no invasiva. Este valor se visualiza en tiempo real a través de la pantalla OLED previamente implementada.

Lo anterior permite obtener lecturas digitales precisas del estado del neonato, facilitando el seguimiento continuo de su crecimiento y desarrollo.

<div align="center">
<img width="464" height="464" alt="image" src="https://github.com/user-attachments/assets/cde06d92-010a-4ab9-be8b-7e2e8eb1130e" />
</div>




El sistema construido se divide en tres componentes principales: electrónica, estructura física y parte eléctrica.


| Componente            | Elementos incluidos                                          | Costo (COP)  |
|----------------------|-------------------------------------------------------------|--------------|
| **Parte electrónica**| DHT22, HX711, capacitores, LM317, resistencias, módulos relé | $60.900      |
| **Caja (estructura)**| Caja plástica (40 × 20 × 22 cm)                             | $20.000      |
| **Parte eléctrica**  | Bombillo de calor, roseta, cableado y enchufe               | $19.500      |
| **TOTAL**            | Sistema completo                                            | **$100.400** |

El costo total del sistema es de **$100.400 COP**, lo cual representa una solución de muy bajo costo frente a equipos médicos reales.

- **Parte electrónica:** ≈ 60.6% del costo total  
- **Estructura (caja):** ≈ 19.9%  
- **Parte eléctrica:** ≈ 19.4%  

### Comparación con incubadoras comerciales

Las incubadoras neonatales comerciales (como las de Dräger, Instrumentalia S.A.S. y LEEX Medical) incluyen características avanzadas como:

- Control de temperatura de alta precisión (PID)
- Sensores múltiples (temperatura, humedad, SpO₂, ECG)
- Control de oxígeno
- Sistemas de humidificación
- Alarmas y seguridad redundante
- Diseño térmico especializado (doble pared)


### Comparación general

| Característica         | Sistema desarrollado | Incubadora comercial                 |
|----------------------|--------------------|------------------------------------|
| Costo                | ~$100.400 COP      | Millones de COP                    |
| Control              | ON/OFF             | PID / avanzado                     |
| Variables            | Temp, peso         | Temp, SpO₂, ECG, humedad, etc.     |
| Seguridad            | Básica             | Alta (alarmas, redundancia)        |
| Certificación        | No                 | Sí                                 |
| Precisión            | Media-baja         | Alta                               |



## PARTE C

```cpp
#include <Wire.h>
#include <U8g2lib.h>
#include "DHT.h"
#include "HX711.h"

// OLED
U8G2_SSD1306_128X64_NONAME_F_HW_I2C 
u8g2(U8G2_R0, U8X8_PIN_NONE, 22, 21);

// DHT22
#define DHTPIN 4
#define DHTTYPE DHT22
DHT dht(DHTPIN, DHTTYPE);

// Relés
#define RELAY1 5
#define RELAY2 18

// LEDs
#define LED_ROJO 25
#define LED_VERDE 26

// HX711
#define DT 19
#define SCK 23
HX711 scale;

bool calefactorON = true;
bool ventiladorON = false;

float factor_calibracion = -7050;

unsigned long tiempoInicio;
bool yaTarado = false;

float temp = 0;

void drawCentered(const char* text, int y) {
  int w = u8g2.getStrWidth(text);
  int x = (128 - w) / 2;
  u8g2.drawStr(x, y, text);
}

void setup() {
  Serial.begin(115200);

  Wire.begin(21, 22);
  u8g2.begin();
  dht.begin();

  pinMode(RELAY1, OUTPUT);
  pinMode(RELAY2, OUTPUT);

  pinMode(LED_ROJO, OUTPUT);
  pinMode(LED_VERDE, OUTPUT);

  digitalWrite(RELAY1, HIGH);
  digitalWrite(RELAY2, LOW);

  digitalWrite(LED_ROJO, LOW);
  digitalWrite(LED_VERDE, LOW);

  scale.begin(DT, SCK);
  scale.set_scale(factor_calibracion);

  tiempoInicio = millis();
}

void loop() {

  // Tara
  if (!yaTarado && millis() - tiempoInicio > 6000) {
    if (scale.is_ready()) {
      scale.tare(15);
      yaTarado = true;
    }
  }

  // Temperatura
  float nuevaTemp = dht.readTemperature();
  if (!isnan(nuevaTemp)) {
    temp = nuevaTemp;
  }

  // Control temperatura
  if (temp < 36) {
    calefactorON = true;
    ventiladorON = false;
  } 
  else if (temp > 37.5) {
    calefactorON = false;
    ventiladorON = true;
  }

  digitalWrite(RELAY1, calefactorON ? HIGH : LOW);
  digitalWrite(RELAY2, ventiladorON ? HIGH : LOW);

  // LED rango 36 - 37.5
  if (temp >= 36 && temp <= 37.5) {
    digitalWrite(LED_ROJO, LOW);
    digitalWrite(LED_VERDE, HIGH);
  } else {
    digitalWrite(LED_ROJO, HIGH);
    digitalWrite(LED_VERDE, LOW);
  }

  // Peso
  float peso = 0;
  if (scale.is_ready()) {
    static float peso_filtrado = 0;
    float lectura = scale.get_units(10);
    peso_filtrado = 0.8 * peso_filtrado + 0.2 * lectura;
    peso = peso_filtrado;
  }

  char tempStr[10];
  char pesoStr[10];

  dtostrf(temp, 4, 1, tempStr);
  dtostrf(peso, 4, 1, pesoStr);

  // OLED
  u8g2.clearBuffer();
  u8g2.setFont(u8g2_font_5x7_tr);

  char linea1[30];
  sprintf(linea1, "Temp: %s C", tempStr);
  drawCentered(linea1, 25);

  char linea2[30];
  sprintf(linea2, "Peso: %s g", pesoStr);
  drawCentered(linea2, 45);

  u8g2.sendBuffer();

  delay(2000);
}
```

Se implementa un sistema embebido que monitorea y controla variables como temperatura y masa, utilizando una plataforma basada en microcontrolador. El sistema integra sensores, actuadores e interfaz de visualización, constituyendo una solución de control en lazo cerrado de tipo ON/OFF con realimentación.

En primer lugar, el sistema adquiere la variable de temperatura mediante un sensor digital DHT22, el cual proporciona mediciones periódicas con una frecuencia aproximada de 0.5 Hz. Para garantizar la validez de los datos, se realiza una verificación mediante la función isnan().

El control de temperatura se basa en una lógica ON/OFF con histéresis, estableciendo un rango de operación entre 36 °C y 37.5 °C. Cuando la temperatura desciende por debajo del límite inferior, se activa el calefactor; por el contrario, cuando supera el límite superior, se activa el sistema de ventilación. Dentro del rango definido, el sistema mantiene el último estado de los actuadores, lo cual evita conmutaciones rápidas y reduce el desgaste de los dispositivos. Este comportamiento corresponde a un controlador tipo disparador de Schmitt, ampliamente utilizado en sistemas donde se desea estabilidad frente a pequeñas perturbaciones.

Para la medición de masa, el sistema emplea un módulo HX711 acoplado a una celda de carga. Se implementa un proceso de tara automática posterior al arranque del sistema, con un retardo de seis segundos para permitir la estabilización de la señal. Adicionalmente, se aplica un filtro digital de tipo pasa-bajos (IIR de primer orden).

Este filtrado reduce significativamente el ruido en la señal de peso, mejorando la estabilidad de la medición y la confiabilidad de los datos mostrados.

El sistema incluye indicadores visuales mediante LEDs para informar el estado de la temperatura. Un LED azul indica que la variable se encuentra dentro del rango de operación, mientras que un LED rojo señala condiciones fuera de especificación. Tambien, se implementa una interfaz gráfica mediante una pantalla OLED, en la cual se muestran los valores de temperatura y peso, mejorando la interacción con el usuario.

### ¿Qué otras variables son críticas en el monitoreo neonatal?

- La humedad relativa es importante porque los neonatos, especialmente los prematuros, presentan una piel inmadura que favorece la pérdida de agua por evaporación. Un control inadecuado de la humedad puede provocar deshidratación y alteraciones en el equilibrio térmico. De hecho, la guía de laboratorio destaca la importancia de evaluar el impacto de variables como la temperatura, la humedad y el flujo de aire en la salud del neonato .

- El flujo de aire, el cual influye directamente en la distribución uniforme de la temperatura dentro de la incubadora. Un flujo inadecuado puede generar gradientes térmicos, afectando la estabilidad del ambiente interno.

- La frecuencia respiratoria constituye un parámetro fisiológico esencial, ya que permite evaluar el estado del sistema respiratorio del neonato. 

- La frecuencia cardíaca es una variable crítica para la evaluación del estado hemodinámico del neonato. Su monitoreo continuo permite detectar eventos como bradicardia o taquicardia, los cuales pueden comprometer la vida del paciente si no se identifican oportunamente.

- La saturación de oxígeno (SpO₂) es indispensable para garantizar una adecuada oxigenación de los tejidos. Niveles bajos pueden indicar hipoxia, mientras que niveles excesivos en neonatos prematuros pueden generar complicaciones como retinopatía del prematuro.

### ¿Qué haría falta para convertir el sistema desarrollado en una incubadora neonatal real?


- Se debería mejorar la precisión y confiabilidad de los sensores. Usar sensores como el DHT22 es bueno para prototipos, pero en aplicaciones clínicas se requieren sensores certificados de grado médico, con alta exactitud, estabilidad y tiempos de respuesta controlados. Asimismo, sería necesario incluir sensores adicionales como humedad relativa, concentración de oxígeno y flujo de aire, variables que, según la guía de laboratorio, influyen directamente en la salud del neonato .

- El sistema de control debe cambiar a controladores PID o adaptativos, que permitan una regulación más precisa y continua de la temperatura. A diferencia del control ON/OFF implementado, estos métodos reducen las oscilaciones y mejoran la estabilidad térmica, lo cual es crítico en neonatos prematuros con limitada capacidad de termorregulación.

- El sistema de seguridad y redundancia ya que debería contar con alarmas auditivas y visuales ante condiciones críticas, así como sistemas redundantes que garanticen el funcionamiento continuo en caso de fallos. 

- En la arquitectura del sistema, se requiere eliminar el uso de retardos bloqueantes y adoptar una programación en tiempo real, permitiendo la ejecución simultánea de múltiples tareas críticas.

### ¿Qué semejanzas hay entre una incubadora neonatal y una servo-cuna?

Ambos dispositivos tienen como objetivo principal mantener la estabilidad térmica del neonato, proporcionando un entorno controlado que compense la limitada capacidad de termorregulación del recién nacido, en segundo lugar, ambos sistemas operan mediante mecanismos de control en lazo cerrado, donde la temperatura medida se compara con un valor de referencia, ajustando la acción de los actuadores para corregir desviaciones. 

La integración de sistemas de monitoreo, que permiten supervisar variables fisiológicas y ambientales relevantes. Tanto la incubadora como la servo-cuna pueden incorporar sensores adicionales (como frecuencia cardíaca, saturación de oxígeno o peso), así como interfaces de visualización para el personal médico, también ambos dispositivos incluyen sistemas de alarma y seguridad, diseñados para alertar sobre condiciones anómalas, como sobrecalentamiento, fallas en sensores o interrupciones en el suministro eléctrico, garantizando la protección del neonato.

## CONCLUSIONES 

- Se comprendió la importancia del control preciso de variables físicas en el cuidado del recién nacido, especialmente en condiciones de vulnerabilidad como la prematuridad. En particular, se evidenció que la temperatura es un factor crítico, ya que pequeñas variaciones pueden comprometer la estabilidad fisiológica del neonato, lo cual justifica la necesidad de sistemas de control confiables y continuos.

- El sistema implementado demostró que es posible emular el funcionamiento básico de una incubadora mediante un esquema de control ON/OFF con histéresis, logrando mantener la temperatura dentro de un rango adecuado. Asimismo, la integración de sensores como el de temperatura y el de peso permitió establecer un sistema de monitoreo funcional, capaz de proporcionar información relevante en tiempo real. El uso de filtrado digital en la señal de masa evidenció la importancia del procesamiento de señales para mejorar la calidad de las mediciones.

- Pero se encontraron limitantes importantes en el sistema desarrollado, como que falta un control avanzado (como PID), la falta de monitoreo de variables adicionales críticas (humedad, oxigenación, frecuencia cardíaca), y el uso de técnicas de programación bloqueantes que limitan el desempeño en tiempo real.

- La implementación de una incubadora neonatal real requiere no solo mejoras técnicas, sino también el cumplimiento de estrictos estándares de seguridad, confiabilidad y certificación. Aspectos como la redundancia de sistemas, la incorporación de alarmas, el uso de sensores de grado médico y el diseño físico adecuado son indispensables para garantizar la protección del paciente.



# REFERENCIAS

- [1] ScienceDirect, "Neonatal Incubator - an overview," ScienceDirect Topics, 2024. [En línea]. Disponible: https://www.sciencedirect.com/topics/nursing-and-health-professions/neonatal-incubator. [Accedido: 23-abr-2026].

- [2] J. Villalobos, "Partes de una incubadora neonatal," Prezi, 2018. [En línea]. Disponible: https://prezi.com/p/l6cj35j2nfv6/partes-de-una-incubadora-neonatal/. [Accedido: 23-abr-2026].




