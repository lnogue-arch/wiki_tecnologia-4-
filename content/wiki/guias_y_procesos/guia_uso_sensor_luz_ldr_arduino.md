---
title: Guía de Uso del Sensor de Luz LDR con Arduino
tags: [guia, ldr, sensor_luz, adc, arduino, 3a_evaluacion, 4eso]
aliases: [Práctica LDR Arduino, Sensor de Oscuridad, Detector de Luz]
---

# Guía de Uso del Sensor de Luz LDR con Arduino

## 1. Montaje del Divisor de Tensión
La fotorresistencia LDR varía su resistencia con la luz, pero los pines analógicos de Arduino solo pueden medir voltajes. Por tanto, es obligatorio montar un **divisor de tensión**:

```text
       +5V (Vcc)
         |
       [ R_fija = 10 kΩ ]
         |
         +-------------------> Conectar a Pin Analógico A0 de Arduino
         |
       [ LDR ]
         |
        GND (0V)
```

* **A plena luz**: La resistencia del LDR baja mucho ($< 1\text{ k}\Omega$), derivando la corriente a GND $\rightarrow$ La tensión en A0 baja hacia $0\text{ V}$ (lectura ADC baja $\approx 50-200$).
* **En oscuridad**: La resistencia del LDR sube a varios cientos de $\text{k}\Omega$ $\rightarrow$ La tensión en A0 sube hacia $+5\text{ V}$ (lectura ADC alta $\approx 800-1023$).

---

## 2. Código de Calibración y Control Automático

```cpp
#define pinLED 12
#define pinLDR A0

int umbralLuz = 500; // Valor de calibración determinado en el monitor serie

void setup() {
  pinMode(pinLED, OUTPUT);
  Serial.begin(9600);
  Serial.println("--- INICIANDO DETECTOR DE LUZ ---");
}

void loop() {
  int valorSensor = analogRead(pinLDR);
  
  // Imprimir valor en el monitor serie para calibrar
  Serial.print("Nivel de luz leído: ");
  Serial.println(valorSensor);

  // Si hay oscuridad (valor por encima del umbral), encender la farola
  if (valorSensor > umbralLuz) {
    digitalWrite(pinLED, HIGH);
  } else {
    digitalWrite(pinLED, LOW);
  }

  delay(200); // Pequeña pausa para no saturar la comunicación serie
}
```

---

## 3. Calibración en el Taller
1. Abre el **Monitor Serie** (`Herramientas -> Monitor Serie` a 9600 baudios).
2. Anota el valor cuando la luz ambiental del aula incide sobre el LDR (ej. $220$).
3. Tapa el LDR con el dedo simulando la noche y anota el nuevo valor (ej. $850$).
4. Establece el umbral en el punto medio:
   $$\text{Umbral} = \frac{220 + 850}{2} = 535$$

---
*Conceptos relacionados: [[resistencias_variables_ldr_ntc_ptc]], [[arquitectura_arduino_y_pines]], [[programacion_arduino_funciones_basicas]].*
