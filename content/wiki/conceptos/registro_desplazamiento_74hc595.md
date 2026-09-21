---
title: Registro de Desplazamiento 74HC595 (Shift Register)
tags: [shift_register, 74hc595, expansion_pines, comunicacion_serie, 3a_evaluacion, 4eso]
aliases: [74HC595, Registro de Turnos, Shift Register, Expansor de Pines]
---

# Registro de Desplazamiento 74HC595 (Shift Register)

## ¿Qué es?
El **74HC595** es un circuito integrado de tipo **registro de desplazamiento de 8 bits con entrada serie y salida en paralelo** (*Serial-In Parallel-Out*, SIPO) que incorpora un registro de almacenamiento (*Latch*).

Permite controlar **8 salidas digitales independientes** utilizando únicamente **3 pines de control** de un microcontrolador (Data, Clock y Latch). Además, permite conectar múltiples chips en cascada (*daisy-chain*) para controlar 16, 24, 32 o más salidas sin consumir pines adicionales de Arduino.

### Pines Clave del 74HC595 (DIP-16):
```text
         +---+-+---+
      Q1 | 1    16 | Vcc (+5V)
      Q2 | 2    15 | Q0 (Salida 0)
      Q3 | 3    14 | DS / SER (Serial Data) -> Pin de datos
      Q4 | 4    13 | OE (Output Enable, activo a GND)
      Q5 | 5    12 | ST_CP / RCLK (Latch Clock) -> Pin de cerrojo
      Q6 | 6    11 | SH_CP / SRCLK (Shift Clock) -> Pin de reloj
      Q7 | 7    10 | MR (Master Reset, activo a Vcc)
     GND | 8     9 | Q7' (Serial Out para encadenar)
         +---------+
```

### Protocolo de Funcionamiento:
1. **Clock (SH_CP / Pin 11)**: Con cada flanco de subida del reloj, el bit presente en **Data (DS / Pin 14)** entra en el registro y desplaza los bits anteriores una posición.
2. **Latch (ST_CP / Pin 12)**: Cuando se activa un flanco de subida en el pin Latch, los 8 bits del registro interno se transfieren a las salidas físicas ($Q_0 - Q_7$) de golpe, evitando parpadeos visibles.

### Función `shiftOut()` de Arduino:
```cpp
shiftOut(dataPin, clockPin, MSBFIRST, valorByte);
```
Donde `valorByte` es un entero de 8 bits ($0$ a $255$ o `B10101010`) que enciende o apaga las salidas correspondientes.

---

## ¿Por qué importa?
1. **Optimización de recursos**: Libera pines del microcontrolador para otros sensores.
2. **Control de matrices de LED y displays**: Esencial para carteles publicitarios luminosos, displays de 7 segmentos múltiples y secuenciadores de iluminación.

---

## ¿Cómo se aplica o relaciona?
* Guía de montaje paso a paso y código completo: [[guia_expansion_pines_74hc595]].
* Experiencias de taller: [[fuente_06_taller_y_proyectos_practicos]].
