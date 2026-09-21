---
title: Circuito Integrado 555 (Temporizador Monoestable y Astable)
tags: [ci_555, temporizador, astable, monoestable, 2a_evaluacion, 4eso]
aliases: [Timer 555, CI 555, 555 Astable, 555 Monoestable, NE555]
---

# Circuito Integrado 555 (Temporizador Monoestable y Astable)

## ¿Qué es?
El **NE555** es uno de los circuitos integrados más populares y versátiles de la historia de la electrónica. Es un temporizador de precisión capaz de generar pulsos únicos calibrados o trenes continuos de oscilación.

### Distribución de Pines (DIP-8):
```text
         +---+-+---+
     GND | 1     8 | Vcc (+5V a +15V)
 TRIGGER | 2  5  7 | DISCHARGE (Descarga)
  OUTPUT | 3  5  6 | THRESHOLD (Umbral)
   RESET | 4  5  5 | CONTROL VOLTAGE
         +---------+
```

### Arquitectura Interna:
* Un divisor de tensión con **3 resistencias idénticas de $5\text{ k}\Omega$** (de ahí su nombre 555) que fijan dos tensiones de referencia: $\frac{1}{3}V_{cc}$ y $\frac{2}{3}V_{cc}$.
* Dos comparadores analógicos de tensión.
* Un Flip-Flop biestable RS.
* Un transistor interno de descarga (pin 7).
* Una etapa de salida de potencia (pin 3) capaz de suministrar o absorber hasta $200\text{ mA}$.

---

## Modos Principales de Funcionamiento:

### 1. Modo Monoestable (Temporizador de Un Solo Disparo)
Permanece en reposo con la salida en nivel bajo ('0'). Al recibir un pulso negativo en el pin 2 (Trigger $< \frac{1}{3}V_{cc}$), la salida pasa a nivel alto ('1') durante un tiempo exacto $T$ determinado por una resistencia externa $R$ y un condensador $C$:

$$T = 1{,}1 \cdot R \cdot C \quad [\text{segundos}]$$

* **Aplicaciones**: Luces de escalera con apagado automático, temporizadores de lavado, eliminación de rebotes de pulsadores.

### 2. Modo Astable (Generador de Reloj / Oscilador Libre)
El circuito no tiene ningún estado estable; la salida conmuta continuamente entre nivel alto ('1') y nivel bajo ('0') sin necesidad de disparo externo.

* **Tiempo en Nivel Alto (Salida en 1, carga de $C$ a través de $R_1 + R_2$)**:
  $$T_{\text{on}} = T_H = \ln(2) \cdot (R_1 + R_2) \cdot C \approx 0{,}693 \cdot (R_1 + R_2) \cdot C$$
* **Tiempo en Nivel Bajo (Salida en 0, descarga de $C$ a través de $R_2$)**:
  $$T_{\text{off}} = T_L = \ln(2) \cdot R_2 \cdot C \approx 0{,}693 \cdot R_2 \cdot C$$
* **Periodo Total ($T$)**:
  $$T = T_H + T_L = 0{,}693 \cdot (R_1 + 2R_2) \cdot C$$
* **Frecuencia de Oscilación ($f$)**:
  $$f = \frac{1}{T} = \frac{1{,}44}{(R_1 + 2R_2) \cdot C} \quad [\text{Hz}]$$

---

## ¿Por qué importa?
1. **Generador de pulsos de reloj**: Proporciona la señal de sincronismo para circuitos secuenciales, contadores y registros.
2. **Generación de sonido y efectos luminosos**: Permite crear sirenas, intermitentes para vehículos y moduladores PWM.

---

## ¿Cómo se aplica o relaciona?
* Guía de montaje práctico y dimensionamiento: [[guia_montaje_y_calculo_timer_555]].
* Diagrama de conexionado en [[pinout_555_y_arduino]].
* Experiencias de taller en [[fuente_06_taller_y_proyectos_practicos]].
