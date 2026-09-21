---
title: Cuaderno Completo de Prácticas de Simulación con Crocodile Clips (Solucionario Oficial)
tags: [guia, crocodile, simulacion, ejercicios, circuitos, electronica_analogica, 1a_evaluacion, 4eso]
aliases: [Solucionario Crocodile 4ESO, Ejercicios Crocodile Corregidos]
---

# Cuaderno Completo de Prácticas de Simulación con Crocodile Clips (Solucionario Oficial)

Solucionario íntegro de las 3 partes de simulación de circuitos electrónicos analógicos y digitales en Crocodile Technology / Crocodile Clips.

---

## ⚡ PARTE 1: Circuitos Básicos y Conmutación

### Ejercicio 1: Encendido Básico de Bombilla
* **Componentes**: Pila de $9	ext{ V}$, interruptor simple SPST, bombilla.
* **Solución**: Conectar en serie la pila, el interruptor y la bombilla. Al cerrar el interruptor, circula corriente y la bombilla se ilumina.

### Ejercicio 2: Accionamiento de Motor Eléctrico
* **Componentes**: Pila, interruptor SPST, motor de CC.
* **Solución**: Al cerrar el interruptor, el motor gira en sentido horario por polarización directa.

### Ejercicio 3: Atenuación Sonora de Zumbador con Resistencia
* **Componentes**: Pila, interruptor, resistencia de $330\,\Omega$, zumbador.
* **Solución**: La resistencia en serie reduce la corriente y caída de tensión en el zumbador, atenuando el volumen sonoro.

### Ejercicio 4: Control Independiente de 2 Bombillas
* **Componentes**: Pila, 2 interruptores simples SPST, 2 bombillas.
* **Solución**: Dos ramas en paralelo, cada una con su propio interruptor en serie con su bombilla.

### Ejercicio 5: Conmutación Simple entre Dos Receptores (SPDT)
* **Componentes**: Pila, conmutador unipolar SPDT, 2 bombillas (A y B).
* **Solución**: El común (COM) del conmutador se conecta a la pila ($+$). La salida 1 va a la bombilla A y la salida 2 a la bombilla B. Nunca pueden estar encendidas a la vez.

### Ejercicio 6: Circuito de Pasillo (Conmutada desde 2 Puntos)
* **Componentes**: Pila, 2 conmutadores SPDT, 1 bombilla.
* **Solución**: El positivo va al COM del conmutador 1. Las dos salidas del conmutador 1 se unen con las dos entradas del conmutador 2 mediante dos líneas de puenteo. El COM del conmutador 2 va a la bombilla, y el retorno a GND.

### Ejercicio 7: Inversión de Giro de Motor con Conmutador Bipolar (DPDT)
* **Componentes**: Pila, conmutador DPDT (dos polos, dos direcciones), motor.
* **Solución**: Las líneas de alimentación ($+$ y $-$) se cruzan en los terminales exteriores del DPDT y los terminales centrales van al motor.

---

## 🧲 PARTE 2: Circuitos Electromecánicos con Relés

### Ejercicio 1: Mando Indirecto de Carga con Relé
* **Componentes**: Pila, pulsador/interruptor simple, relé SPDT, bombilla.
* **Solución**: El interruptor alimenta la bobina del relé. El contacto normalmente abierto (NO) del relé cierra el circuito independiente de la bombilla al energizarse.

### Ejercicio 2: Motor Funcionando en Reposo
* **Componentes**: Pila, interruptor, relé SPDT, motor.
* **Solución**: Conectar el motor a través del contacto **Normalmente Cerrado (NC)**. El motor gira en reposo y se detiene cuando el relé es activado.

### Ejercicio 3: Alternancia Automática entre 2 Bombillas con Relé
* **Componentes**: Pila, interruptor, relé SPDT, 2 bombillas (Verde y Roja).
* **Solución**: Bombilla Verde conectada al contacto NC (encendida en reposo). Bombilla Roja conectada al contacto NO (se enciende al pulsar el interruptor).

### Ejercicio 5: Inversión de Giro de Motor Mediante Relé DPDT
* **Componentes**: Pila, interruptor de mando, relé de 2 circuitos y 2 posiciones (DPDT), motor.
* **Solución**: La bobina conmuta simultáneamente los dos contactos cruzados de alimentación, invirtiendo el sentido de giro del motor.

---

## 💡 PARTE 3: Semiconductores, Sensores y Control Electrónico

### Ejercicio 1: Protección de Diodo LED
* **Componentes**: Pila de $9	ext{ V}$, interruptor, resistencia limitadora de $470\,\Omega$, LED.
* **Solución**: La resistencia protege al LED de quemarse ($R = rac{9 - 2}{0{,}015} pprox 470\,\Omega$).

### Ejercicio 2: Regulador de Brillo con Potenciómetro
* **Componentes**: Pila, potenciómetro de $10	ext{ k}\Omega$, resistencia de seguridad de $220\,\Omega$, LED.
* **Solución**: Al girar el cursor del potenciómetro varía la resistencia total y la intensidad, regulando el brillo suavemente.

### Ejercicio 6: Farola Automática con Transistor y LDR
* **Componentes**: Pila de $9	ext{ V}$, divisor de tensión con LDR y potenciómetro, transistor BJT, resistencia de colector y LED.
* **Solución**:
  * En luz: La resistencia del LDR es baja, la tensión en la base no supera los $0{,}7	ext{ V}$, el transistor está en **Corte** y el LED apagado.
  * En oscuridad: La resistencia del LDR aumenta mucho, la tensión en la base sube $>0{,}7	ext{ V}$, el transistor entra en **Saturación** y el LED se enciende automáticamente.

### Ejercicio 7: Alarma de Incendios con Termistor NTC y Transistor
* **Componentes**: Pila, termistor NTC, potenciómetro de calibración, transistor BJT, zumbador.
* **Solución**: Al aumentar la temperatura por fuego, la resistencia del NTC disminuye, polarizando la base del transistor en saturación y haciendo sonar el zumbador.

### Ejercicio 9: Control de Potencia Combinado (LDR + Transistor + Relé)
* **Componentes**: Pila de control, LDR, transistor BJT, diodo volante 1N4007, relé SPDT, bombilla de alta potencia.
* **Solución**: El transistor amplifica la señal del sensor LDR para excitar la bobina del relé, el cual conmuta la bombilla de gran consumo con total aislamiento galvánico.

---
*Conceptos relacionados: [[transistor_bjt_corte_activa_saturacion]], [[rele_electromecanico]], [[resistencias_variables_ldr_ntc_ptc]], [[circuitos_conmutacion_y_control_con_reles]].*
