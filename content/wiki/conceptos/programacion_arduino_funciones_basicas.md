---
title: Programación Arduino (Estructura y Funciones Básicas)
tags: [arduino, programacion, c_cpp, 3a_evaluacion, 4eso]
aliases: [Código Arduino, Sketch Arduino, pinMode, digitalWrite, analogRead]
---

# Programación Arduino (Estructura y Funciones Básicas)

## ¿Qué es?
La programación en Arduino se realiza mediante un lenguaje basado en **C/C++**. Todo programa (denominado *sketch*) consta de dos bloques obligatorios:

```cpp
void setup() {
  // Se ejecuta UNA SOLA VEZ al alimentar o resetear la placa.
  // Se utiliza para configurar pines, iniciar comunicaciones, etc.
}

void loop() {
  // Se ejecuta en un BUCLE INFINITO y continuo.
  // Contiene la lógica central de control, lectura y actuación.
}
```

### Funciones y Comandos Fundamentales:

| Función | Parámetros y Sintaxis | Descripción |
| :--- | :--- | :--- |
| **`pinMode()`** | `pinMode(pin, modo)` (`INPUT`, `OUTPUT`, `INPUT_PULLUP`) | Configura un pin digital como entrada o salida. |
| **`digitalWrite()`** | `digitalWrite(pin, valor)` (`HIGH` o `LOW`) | Envía $5\text{ V}$ o $0\text{ V}$ a un pin digital de salida. |
| **`digitalRead()`** | `digitalRead(pin)` | Lee el estado lógico de una entrada ($HIGH=1$ o $LOW=0$). |
| **`analogRead()`** | `analogRead(pin_analogico)` (A0 - A5) | Lee una tensión de $0-5\text{ V}$ y devuelve un entero entre $0$ y $1023$. |
| **`analogWrite()`** | `analogWrite(pin_pwm, valor)` ($0$ a $255$) | Genera una señal PWM (control de brillo LED o velocidad de motor). |
| **`delay()`** | `delay(milisegundos)` | Pausa la ejecución del programa durante el tiempo indicado ($1000 = 1\text{ s}$). |
| **`Serial.begin()`** | `Serial.begin(9600)` | Inicializa la comunicación serie con el ordenador a 9600 baudios. |
| **`Serial.println()`**| `Serial.println(variable)` | Envía un texto o valor al monitor serie con salto de línea. |

---

## ¿Por qué importa?
Permite transformar algoritmos de control lógico en acciones físicas automáticas sobre motores, relés y señalización.

---

## ¿Cómo se aplica o relaciona?
* Aplicación práctica en semáforos: [[guia_programacion_arduino_semaforos]].
* Lectura de sensores en [[guia_uso_sensor_luz_ldr_arduino]].
* Simulación sin hardware físico en [[guia_simulacion_tinkercad_circuits]].
