---
title: Guía de Expansión de Salidas con Registro 74HC595 y Arduino
tags: [guia, 74hc595, shift_register, expansion_pines, 3a_evaluacion, 4eso]
aliases: [Práctica 74HC595, Secuencia 8 LEDs, shiftOut Arduino]
---

# Guía de Expansión de Salidas con Registro 74HC595 y Arduino

## 1. Conexiones entre Arduino y 74HC595

| Pin Arduino | Pin 74HC595 | Función |
| :--- | :--- | :--- |
| **Pin 4** | **Pin 14 (DS / SER)** | Línea de Datos serie |
| **Pin 5** | **Pin 12 (ST_CP / RCLK)** | Cerrojo / Latch Clock |
| **Pin 6** | **Pin 11 (SH_CP / SRCLK)** | Reloj de desplazamiento / Shift Clock |
| **5V** | **Pin 16 (Vcc)** y **Pin 10 (MR)** | Alimentación y Reset deshabilitado |
| **GND** | **Pin 8 (GND)** y **Pin 13 (OE)** | Masa y Salidas habilitadas |
| Salidas $Q_0 - Q_7$ | **Pines 15, 1, 2, 3, 4, 5, 6, 7** | A cada uno de los 8 LEDs con resistencia de $220\,\Omega$ |

---

## 2. Código Arduino: Secuenciador y Patrones Binarios

```cpp
const int dataPin = 4;   // Pin 14 en 74HC595
const int latchPin = 5;  // Pin 12 en 74HC595
const int clockPin = 6;  // Pin 11 en 74HC595

void setup() {
  pinMode(dataPin, OUTPUT);
  pinMode(latchPin, OUTPUT);
  pinMode(clockPin, OUTPUT);
}

// Función auxiliar para enviar un byte a las 8 salidas
void actualizarLEDs(byte patron) {
  digitalWrite(latchPin, LOW); // Abrir cerrojo
  shiftOut(dataPin, clockPin, MSBFIRST, patron); // Enviar los 8 bits
  digitalWrite(latchPin, HIGH); // Cerrar cerrojo (actualiza las salidas al instante)
}

void loop() {
  // Efecto 1: Barrido de un solo LED (Knight Rider / El Coche Fantástico)
  for (int i = 0; i < 8; i++) {
    byte patron = 1 << i; // Desplaza un '1' binario a la posición i
    actualizarLEDs(patron);
    delay(100);
  }
  for (int i = 6; i > 0; i--) {
    byte patron = 1 << i;
    actualizarLEDs(patron);
    delay(100);
  }

  // Efecto 2: Barra de progreso acumulativa
  byte acumulado = 0;
  for (int i = 0; i < 8; i++) {
    acumulado |= (1 << i);
    actualizarLEDs(acumulado);
    delay(150);
  }
  delay(300);
  actualizarLEDs(0x00); // Apagar todo
  delay(300);
}
```

---
*Conceptos relacionados: [[registro_desplazamiento_74hc595]], [[sistemas_numeracion_binario_hexadecimal]], [[arquitectura_arduino_y_pines]].*
