---
title: Guía de Cálculo y Montaje del Circuito Temporizador 555
tags: [guia, ci_555, taller, protoboard, 2a_evaluacion, 4eso]
aliases: [Montaje 555, Cálculo Frecuencia 555, Práctica 555]
---

# Guía de Cálculo y Montaje del Circuito Temporizador 555

## 1. Diseño en Modo Astable (Generador de Reloj / Oscilador)

### Esquema de Conexionado:
* **Pin 1 (GND)**: Conectar a masa (0V).
* **Pin 8 (Vcc)**: Conectar a $+5\text{V} \dots +12\text{V}$.
* **Pin 4 (RESET)**: Conectar a Vcc (para habilitar el chip).
* **Pin 5 (Control)**: Conectar a GND mediante condensador cerámico de $10\text{ nF}$ (filtro de ruido).
* **Resistencia $R_1$**: Conectada entre Pin 8 (Vcc) y Pin 7 (Discharge).
* **Resistencia $R_2$**: Conectada entre Pin 7 (Discharge) y Pin 6 (Threshold).
* **Puente**: Unir Pin 6 (Threshold) con Pin 2 (Trigger).
* **Condensador $C$**: Conectado entre Pin 2/6 y GND (¡Cuidar polaridad si es electrolítico!).
* **Pin 3 (Salida)**: Conectar el ánodo de un LED con su resistencia de protección de $330\,\Omega$ hacia GND.

### Fórmulas de Cálculo:
$$T_H = 0{,}693 \cdot (R_1 + R_2) \cdot C \quad (\text{tiempo LED encendido})$$
$$T_L = 0{,}693 \cdot R_2 \cdot C \quad (\text{tiempo LED apagado})$$
$$T_{\text{total}} = T_H + T_L = 0{,}693 \cdot (R_1 + 2R_2) \cdot C$$
$$f = \frac{1}{T_{\text{total}}} = \frac{1{,}44}{(R_1 + 2R_2) \cdot C}$$

### Dimensionamiento para Frecuencia $f \approx 1\text{ Hz}$ (Intermitente de 1 segundo):
1. Elegimos $C = 10\,\mu\text{F} = 10 \cdot 10^{-6}\text{ F}$.
2. Escogemos $R_2 = 47\text{ k}\Omega = 47000\,\Omega$.
3. Despejamos $R_1$:
   $$R_1 = \frac{1{,}44}{f \cdot C} - 2R_2 = \frac{1{,}44}{1 \cdot 10^{-5}} - 94000 = 144000 - 94000 = 50\text{ k}\Omega$$
4. Seleccionamos el valor comercial más cercano: **$R_1 = 47\text{ k}\Omega$** o **$56\text{ k}\Omega$**.

---

## 2. Diseño en Modo Monoestable (Temporizador de Escalera)

### Esquema de Conexionado:
* **Pin 2 (Trigger)**: Conectado a Vcc mediante resistencia *pull-up* de $10\text{ k}\Omega$, y con un pulsador normalmente abierto hacia GND.
* **Pin 6 y Pin 7**: Unidos entre sí, conectados a Vcc mediante $R$ y a GND mediante $C$.
* **Pin 3**: Salida hacia relé o LED.

### Fórmula de Duración del Pulso:
$$T = 1{,}1 \cdot R \cdot C$$

### Dimensionamiento para $T = 5\text{ segundos}$:
1. Elegimos $C = 100\,\mu\text{F} = 100 \cdot 10^{-6}\text{ F}$.
2. Despejamos $R$:
   $$R = \frac{T}{1{,}1 \cdot C} = \frac{5}{1{,}1 \cdot 10^{-4}} \approx 45454\,\Omega \approx 47\text{ k}\Omega$$
3. Montando $R = 47\text{ k}\Omega$ y $C = 100\,\mu\text{F}$, el tiempo real será:
   $$T = 1{,}1 \cdot 47000 \cdot 10^{-4} = 5{,}17\text{ s}$$

---
*Conceptos relacionados: [[circuito_integrado_555_monoestable_astable]], [[condensadores_y_constante_rc]], [[pinout_555_y_arduino]].*
