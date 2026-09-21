---
title: "Fuente: Materiales de 3ª Evaluación (Robótica, Arduino y Neumática)"
tags: [fuentes, 3a_evaluacion, robotica, neumatica, arduino, 4eso]
---

# Materiales de 3ª Evaluación (Robótica, Arduino y Neumática)

## Directorios y Archivos de Origen
* Carpeta: `TECNOLOGIA4º/03 tecnología 3 evaluación/`
* Carpeta: `TECNOLOGIA4º/04 EXÁMENES/3ªEVALUACIÓN/`
  * `EXAMEN (TECNOLOGÍA 3ªEV).docx`
  * `CORRECCIÓN TECN 4ESO3ªev.docx` / `CORRECCIÓN TECN 4ESO3ªev.pdf`
* Carpeta: `TECNOLOGIA4º/06 TALLER TODO EL CURSO/`
  * `taller 3ª eval_arduino-20240609T102614Z-001.zip`
    * `Detector de luz.docx`
    * `Cómo funciona el registro de turnos 74HC595 def.docx`
    * `Cómo funciona el registro de turnos 74HC595.docx`
    * Prácticas entregadas de LDR y Secuencias de LEDs
  * `arduino_tinkercad-20240609T102709Z-001.zip`
    * `TINKERCAD CON ARDUINO.pptx`
    * Actividades de cruce semafórico y servos

---

## Síntesis de Contenidos Ingeridos
1. **Robótica y Control**:
   * Definición formal de robot y clasificación según arquitectura (poliarticulados, móviles, androides, zoomórficos, híbridos).
   * Sistemas de control: Lazo abierto (sin realimentación, temporizado) vs Lazo cerrado (con sensores de feedback y corrección de error).
2. **Plataforma Arduino y Sensores**:
   * Hardware de Arduino UNO (microcontrolador ATmega328P, pines digitales, PWM, analógicos ADC de 10 bits).
   * Sensor de luz LDR montado en divisor de tensión con calibración analógica.
   * Registro de desplazamiento 74HC595 (SIPO 8 bits) mediante líneas Data, Latch y Clock con función `shiftOut()`.
3. **Neumática e Hidráulica**:
   * Magnitudes físicas: Fuerza, sección y presión ($P = F/S$ en Pa y bar).
   * Principio de Pascal aplicado a prensas hidráulicas ($F_1/S_1 = F_2/S_2$).
   * Dinámica de fluidos: Caudal ($Q = S \cdot v$) y Ecuación de Continuidad ($S_1 v_1 = S_2 v_2$).
   * Elementos del circuito: Compresor, depósito de aire y Unidad de Mantenimiento FRL (Filtro, Regulador con manómetro y Lubricador).
   * Válvulas distribuidoras ($2/2, 3/2, 5/2$) y actuadores (cilindros de simple y doble efecto).
   * Válvulas lógicas: Válvula de simultaneidad (función lógica "Y" / AND) y Válvula selectora (función lógica "O" / OR).

---
*Conceptos desarrollados: [[robotica_y_sistemas_control]], [[arquitectura_arduino_y_pines]], [[programacion_arduino_funciones_basicas]], [[registro_desplazamiento_74hc595]], [[neumatica_fuerza_presion_pascal]], [[caudal_y_ecuacion_continuidad]], [[circuito_neumatico_frl_compresor]], [[valvulas_distribuidoras_neumaticas]], [[valvulas_logicas_simultaneidad_selectora]].*
