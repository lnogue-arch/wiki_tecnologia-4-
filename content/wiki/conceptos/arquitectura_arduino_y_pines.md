---
title: Arquitectura Arduino y Mapa de Pines (Hardware)
tags: [arduino, hardware, microcontroladores, 3a_evaluacion, 4eso]
aliases: [Arduino UNO, Pines Arduino, Hardware Arduino, ATmega328P]
---

# Arquitectura Arduino y Mapa de Pines (Hardware)

## ¿Qué es?
**Arduino UNO** es una plataforma de hardware libre basada en el microcontrolador **ATmega328P** de Microchip/Atmel. Integra en una única placa de circuito impreso todo lo necesario para interactuar con sensores y actuadores:

### Distribución de Recursos Hardware:
* **Microcontrolador**: ATmega328P (arquitectura Harvard AVR de 8 bits a $16\text{ MHz}$, 32 KB Flash, 2 KB SRAM, 1 KB EEPROM).
* **Pines Digitales (0 a 13)**: 
  * Pueden configurarse como entradas (`INPUT`) o salidas (`OUTPUT`).
  * Nivel de tensión: $0\text{ V}$ (LOW) y $+5\text{ V}$ (HIGH). Corriente máxima por pin: $20\text{ mA}$ (máximo absoluto $40\text{ mA}$).
  * **Pines PWM (Pulse Width Modulation)**: Marcados con una tilde (**~**): pines **3, 5, 6, 9, 10 y 11**. Permiten simular salidas analógicas mediante modulación por ancho de pulsos ($0$ a $255$).
  * **Pines UART Serie**: Pin 0 (RX - Recepción) y Pin 1 (TX - Transmisión). Conectados al chip de comunicación USB.
  * **Pin 13**: Conectado internamente a un LED SMD integrado (marcado con una 'L').
* **Pines Analógicos (A0 a A5)**:
  * Entradas analógicas conectadas a un Convertidor Analógico-Digital (**ADC**) de 10 bits ($2^{10} = 1024$ niveles de resolución, cuantificando tensiones de $0\text{ V}$ a $5\text{ V}$ en valores enteros de $0$ a $1023$).
  * También pueden funcionar como pines digitales estándar si fuera necesario.
* **Pines de Alimentación**:
  * **5V**: Salida regulada a $5\text{ V}$.
  * **3.3V**: Salida regulada a $3{,}3\text{ V}$ (máx. $50\text{ mA}$).
  * **GND**: Terminales de masa común / 0V (3 pines disponibles).
  * **Vin**: Entrada de alimentación externa no regulada ($7\text{ V} - 12\text{ V}$).
  * **RESET**: Reinicia el microcontrolador al conectarse a GND.

---

## ¿Por qué importa?
1. **Facilidad de prototipado**: Permite crear prototipos funcionales de robótica y domótica sin tener que diseñar placas de circuito impreso desde cero.
2. **Entorno educativo universal**: Es el estándar docente en centros educativos de todo el mundo.

---

## ¿Cómo se aplica o relaciona?
* Consulta las funciones software en [[programacion_arduino_funciones_basicas]].
* Expansión de pines de salida con [[registro_desplazamiento_74hc595]].
* Prácticas guiadas: [[guia_programacion_arduino_semaforos]] y [[guia_uso_sensor_luz_ldr_arduino]].
