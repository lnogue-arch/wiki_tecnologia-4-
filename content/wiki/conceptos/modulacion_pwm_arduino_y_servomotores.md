---
title: Modulación por Ancho de Pulsos (PWM) y Control de Servomotores con Arduino
tags: [arduino, pwm, servomotor, control_analogico, 3a_evaluacion, 4eso]
aliases: [PWM Arduino, analogWrite, Control de Servomotores, Librería Servo.h, Ciclo de Trabajo]
---

# Modulación por Ancho de Pulsos (PWM) y Control de Servomotores con Arduino

## 1. Modulación por Ancho de Pulsos (PWM - Pulse Width Modulation)

### ¿Qué es?
Los microcontroladores digitales como el ATmega328P de Arduino solo pueden emitir tensiones binarias ($0	ext{ V}$ o $5	ext{ V}$). Para simular una tensión analógica intermedia (por ejemplo, regular el brillo de un LED o la velocidad de un motor eléctrico de CC), se utiliza la técnica **PWM**: se conmuta la salida digital entre nivel ALTO y BAJO a muy alta frecuencia ($pprox 490	ext{ Hz}$ o $980	ext{ Hz}$) variando el **ciclo de trabajo (*duty cycle*)**.

```text
 0% Duty Cycle (0V continuo):     _________________________  -> analogWrite(pin, 0)
25% Duty Cycle (1.25V efectivo):  --|______--|______--|_____  -> analogWrite(pin, 64)
50% Duty Cycle (2.5V efectivo):   ---|---|---|---|---|---|--  -> analogWrite(pin, 127)
75% Duty Cycle (3.75V efectivo):  ------|--|------|--|------  -> analogWrite(pin, 191)
100% Duty Cycle (5V continuo):    -------------------------  -> analogWrite(pin, 255)
```

### Pines PWM en Arduino UNO:
Están identificados en la serigrafía de la placa con una tilde (**~**):
* **Pines: 3, 5, 6, 9, 10 y 11**.

### Función `analogWrite()`:
```cpp
analogWrite(pin_pwm, valor); // valor entero de 8 bits entre 0 (apagado) y 255 (máximo)
```

---

## 2. Servomotores de Modelismo (Servos de $0^\circ$ a $180^\circ$)

### ¿Qué es?
Un **servomotor** es un actuador rotativo que integra en un único bloque:
1. Un motor eléctrico de CC de alta velocidad.
2. Una caja reductora de engranajes para multiplicar el par de fuerza.
3. Un potenciómetro interno solidario al eje para medir la posición real.
4. Un circuito de control en lazo cerrado [[robotica_y_sistemas_control]] que ajusta el eje al ángulo exacto comandado.

### Conexión del Cable del Servomotor (3 hilos):
* **Marrón / Negro**: Masa (**GND**).
* **Rojo**: Alimentación positiva (**$+5	ext{V}$**).
* **Naranja / Amarillo**: Señal de control PWM (conectar a un pin digital de Arduino, ej. Pin 9).

### Programación con la Librería `<Servo.h>` y Mapeo:
```cpp
#include <Servo.h>

Servo miServo; // Crear objeto servo
const int pinPotenciometro = A0;

void setup() {
  miServo.attach(9); // Asociar el pin digital 9 al servo
}

void loop() {
  int lecturaADC = analogRead(pinPotenciometro); // 0 a 1023
  // La función map convierte linealmente el rango del sensor al rango angular
  int angulo = map(lecturaADC, 0, 1023, 0, 180);
  
  miServo.write(angulo); // Posicionar el servomotor en el ángulo deseado
  delay(15);             // Breve pausa para dar tiempo al movimiento mecánico
}
```

---

## ¿Por qué importa?
Permite el posicionamiento angular milimétrico de articulaciones de brazos robóticos, timones de aeromodelismo, barreras de peaje y cámaras robotizadas.

---

## ¿Cómo se aplica o relaciona?
* Práctica guiada detallada en [[guia_completa_practicas_arduino_tinkercad]].
* Conceptos de hardware en [[arquitectura_arduino_y_pines]].
