---
title: Guía Completa de Prácticas de Robótica con Arduino y Tinkercad (Prácticas 00 a 09)
tags: [guia, arduino, tinkercad, robotica, programacion, 3a_evaluacion, 4eso]
aliases: [Prácticas Arduino 4ESO, Manual Tinkercad Arduino, Guía Tinkercad 4º ESO]
---

# Guía Completa de Prácticas de Robótica con Arduino y Tinkercad (Prácticas 00 a 09)

Manual oficial de prácticas de laboratorio y simulación virtual en Autodesk Tinkercad Circuits.

---

## Índice de Prácticas
* **Práctica 00.1**: La placa Arduino UNO y su mapa de conexiones.
* **Práctica 00.2**: Arduino como fuente de alimentación ($5	ext{V}$ y GND en protoboard).
* **Práctica 00.3**: Práctica 0 - Encendido y parpadeo de un LED (*Blink*).
* **Práctica 01**: Semáforo básico de 3 colores con temporización secuencial.
* **Práctica 02**: Cruce de dos semáforos sincronizados con pulsador peatonal.
* **Práctica 03**: Secuencia luminosa "Coche Fantástico" (*Knight Rider*) con array de LEDs.
* **Práctica 04**: Control de luminosidad de un LED mediante **PWM** (`analogWrite`).
* **Práctica 05**: Luminosidad aleatoria de LED simulando el parpadeo de una vela (`random`).
* **Práctica 06**: Farola automática con sensor de luz **LDR** y divisor de tensión.
* **Práctica 07**: Sistema de alarma sonora y visual con zumbador piezoeléctrico (`tone`/`noTone`).
* **Práctica 08**: Control de ángulo de un **Servomotor** ($0^\circ - 180^\circ$) con potenciómetro (`Servo.h` y `map`).
* **Práctica 09**: Simulación y control de circuitos neumáticos y electroneumáticos.

---

## 🛠️ Desarrollo Detallado de Prácticas

### Práctica 00: Encendido y Parpadeo de un LED (Blink)
* **Objetivo**: Comprender la estructura de un sketch en C++ (`setup` y `loop`) y las funciones digitales básicas.
* **Montaje**: Ánodo del LED al Pin 13 de Arduino, Cátodo a una resistencia de $220\,\Omega$ y de ahí a GND.
* **Código C++**:
```cpp
void setup() {
  pinMode(13, OUTPUT); // Pin 13 configurado como salida digital
}

void loop() {
  digitalWrite(13, HIGH); // Envía 5V al LED (se enciende)
  delay(1000);            // Pausa de 1 segundo (1000 ms)
  digitalWrite(13, LOW);  // Envía 0V al LED (se apaga)
  delay(1000);            // Pausa de 1 segundo
}
```

---

### Práctica 03: Secuencia "Coche Fantástico" (Knight Rider)
* **Objetivo**: Controlar 5 o más LEDs consecutivos utilizando bucles `for` y arrays de pines.
* **Pines**: LEDs en pines digitales 2, 3, 4, 5 y 6 con resistencias individuales de $220\,\Omega$.
* **Código C++**:
```cpp
const int pinesLED[] = {2, 3, 4, 5, 6};
const int numLEDs = 5;

void setup() {
  for (int i = 0; i < numLEDs; i++) {
    pinMode(pinesLED[i], OUTPUT);
  }
}

void loop() {
  // Barrido hacia la derecha
  for (int i = 0; i < numLEDs; i++) {
    digitalWrite(pinesLED[i], HIGH);
    delay(80);
    digitalWrite(pinesLED[i], LOW);
  }
  // Barrido de retorno hacia la izquierda
  for (int i = numLEDs - 2; i > 0; i--) {
    digitalWrite(pinesLED[i], HIGH);
    delay(80);
    digitalWrite(pinesLED[i], LOW);
  }
}
```

---

### Práctica 04: Regulación de Luminosidad por PWM
* **Objetivo**: Utilizar la modulación por ancho de pulsos en el Pin 9 (~PWM) para regular gradualmente el brillo del LED.
* **Código C++**:
```cpp
const int pinLED = 9;

void setup() {
  pinMode(pinLED, OUTPUT);
}

void loop() {
  // Aumentar brillo progresivamente (0 a 255)
  for (int brillo = 0; brillo <= 255; brillo += 5) {
    analogWrite(pinLED, brillo);
    delay(20);
  }
  // Disminuir brillo progresivamente (255 a 0)
  for (int brillo = 255; brillo >= 0; brillo -= 5) {
    analogWrite(pinLED, brillo);
    delay(20);
  }
}
```

---

### Práctica 05: Luminosidad Aleatoria (Efecto Llama de Vela)
* **Objetivo**: Generar valores pseudoaleatorios con la función `random(min, max)` para simular la luz fluctuante de una llama.
* **Código C++**:
```cpp
const int pinLED = 9; // Pin PWM

void setup() {
  pinMode(pinLED, OUTPUT);
}

void loop() {
  int nivelAleatorio = random(50, 255); // Genera un valor de brillo entre 50 y 255
  analogWrite(pinLED, nivelAleatorio);
  delay(random(30, 150)); // Tiempo de destello variable
}
```

---

### Práctica 06: Farola Automática con Sensor LDR
* **Objetivo**: Lectura analógica por Pin A0 mediante divisor de tensión ($10	ext{ k}\Omega + 	ext{LDR}$) y activación nocturna automática.
* **Código C++**:
```cpp
const int pinLDR = A0;
const int pinFarola = 8;
const int umbralNoche = 500;

void setup() {
  pinMode(pinFarola, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int valorLuz = analogRead(pinLDR);
  Serial.println(valorLuz);
  
  if (valorLuz > umbralNoche) {
    digitalWrite(pinFarola, HIGH); // Oscuridad detectada -> Enciende farola
  } else {
    digitalWrite(pinFarola, LOW);  // Luz diurna -> Apaga farola
  }
  delay(100);
}
```

---

### Práctica 07: Alarma Sonora y Visual con Zumbador Piezoeléctrico
* **Objetivo**: Generar tonos de audio con la función `tone(pin, frecuencia_Hz)` acompañados de destellos luminosos.
* **Código C++**:
```cpp
const int pinBuzzer = 7;
const int pinLEDRojo = 6;
const int pinPulsador = 2;

void setup() {
  pinMode(pinBuzzer, OUTPUT);
  pinMode(pinLEDRojo, OUTPUT);
  pinMode(pinPulsador, INPUT_PULLUP); // Pulsador a GND
}

void loop() {
  if (digitalRead(pinPulsador) == LOW) { // Intrusión / Pulsador presionado
    digitalWrite(pinLEDRojo, HIGH);
    tone(pinBuzzer, 1000); // Tono de 1000 Hz
    delay(250);
    digitalWrite(pinLEDRojo, LOW);
    tone(pinBuzzer, 500);  // Tono de 500 Hz (efecto sirena)
    delay(250);
  } else {
    noTone(pinBuzzer);
    digitalWrite(pinLEDRojo, LOW);
  }
}
```

---

### Práctica 08: Control Angular de Servomotor con Potenciómetro
* **Objetivo**: Controlar la posición angular ($0^\circ - 180^\circ$) de un servomotor en tiempo real mediante un potenciómetro en A0.
* **Código C++**:
```cpp
#include <Servo.h>

Servo servomotor;
const int pinPot = A0;

void setup() {
  servomotor.attach(9); // Pin PWM 9
}

void loop() {
  int valorPot = analogRead(pinPot);             // Rango 0 - 1023
  int angulo = map(valorPot, 0, 1023, 0, 180);   // Conversión a 0 - 180 grados
  servomotor.write(angulo);
  delay(15);
}
```

---
*Conceptos relacionados: [[arquitectura_arduino_y_pines]], [[programacion_arduino_funciones_basicas]], [[modulacion_pwm_arduino_y_servomotores]], [[guia_simulacion_tinkercad_circuits]].*
