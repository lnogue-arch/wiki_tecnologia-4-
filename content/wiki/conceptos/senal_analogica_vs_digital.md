---
title: Señal Analógica vs Señal Digital
tags: [electronica_digital, fundamentos, teoria_senales, 2a_evaluacion, 4eso]
aliases: [Señal Analógica, Señal Digital, Comparativa Señales]
---

# Señal Analógica vs Señal Digital

## ¿Qué es?
Las señales eléctricas son variaciones de tensión o corriente que transportan información:

### 1. Señal Analógica
* Es una magnitud **continua en el tiempo** que puede tomar **infinitos valores** dentro de un rango determinado.
* *Ejemplos*: La voz humana captada por un micrófono, la temperatura ambiental leída por un termistor, la intensidad luminosa natural, la señal de radio FM tradicional.

### 2. Señal Digital
* Es una magnitud **discreta tanto en el tiempo como en la amplitud**, que solo puede adoptar un número finito de estados bien definidos.
* En la electrónica binaria convencional se emplean **dos niveles lógicos**:
  * **'0' Lógico (Nivel Bajo / LOW)**: Representado habitualmente por $0\text{ V}$ (rango $0\text{ V} - 0{,}8\text{ V}$ en lógica TTL).
  * **'1' Lógico (Nivel Alto / HIGH)**: Representado por $+5\text{ V}$ o $+3{,}3\text{ V}$ (rango $2\text{ V} - 5\text{ V}$ en TTL).

### Tabla Comparativa de Características:

| Criterio | Señal Analógica | Señal Digital |
| :--- | :--- | :--- |
| **Valores posibles** | Infinitos (continuos) | Dos niveles discretos ('0' y '1') |
| **Inmunidad al ruido** | Muy baja (el ruido distorsiona la información) | Muy alta (el ruido debe ser enorme para cambiar un 0 a 1) |
| **Almacenamiento** | Complejo y con degradación (cintas magnéticas) | Sencillo, exacto y sin pérdidas (memorias flash, SSD) |
| **Procesamiento** | Requiere filtros complejos de hardware | Altamente programable mediante software y microcontroladores |
| **Transmisión a larga distancia** | Se degrada progresivamente | Se regenera perfectamente mediante repetidores |

---

## ¿Por qué importa?
1. **Revolución Digital**: Toda la tecnología moderna (smartphones, ordenadores, internet, streaming) se fundamenta en la digitalización de la información analógica del mundo real.
2. **Conversores ADC y DAC**: Permite entender la necesidad del convertidor Analógico-Digital (ADC) integrado en [[arquitectura_arduino_y_pines]] para leer sensores analógicos.

---

## ¿Cómo se aplica o relaciona?
* Interfaz con sistemas numéricos binarios: [[sistemas_numeracion_binario_hexadecimal]].
* Base para el análisis de [[puertas_logicas_fundamentales]].
