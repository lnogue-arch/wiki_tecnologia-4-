---
title: Relé Electromecánico y Aislamiento Galvánico
tags: [actuadores, potencia, aislamiento, 1a_evaluacion, 4eso]
aliases: [Relé, Relay, Contactos COM NO NC]
---

# Relé Electromecánico y Aislamiento Galvánico

## ¿Qué es?
Un **relé electromecánico** es un interruptor accionado magnéticamente. Consta de dos partes completamente aisladas entre sí:
1. **Circuito de excitación o control**: Una bobina de hilo de cobre enrollada sobre un núcleo de hierro dulce (funciona a baja tensión: $5\text{ V}, 12\text{ V}$ o $24\text{ V DC}$).
2. **Circuito de potencia o fuerza**: Uno o varios contactos mecánicos capaces de conmutar tensiones y corrientes elevadas ($230\text{ V AC}, 10\text{ A}$).

### Estructura de Terminales de Salida:
* **COM (Común)**: Borne principal de entrada de la línea de potencia.
* **NC (Normally Closed / Normalmente Cerrado)**: Hace contacto con COM cuando la bobina **NO** recibe corriente.
* **NO / NA (Normally Open / Normalmente Abierto)**: Hace contacto con COM cuando la bobina **SÍ** recibe corriente y se magnetiza.

### Diodo Volante (Flyback Diode):
Cuando se corta la corriente de la bobina del relé, el campo magnético colapsa bruscamente, induciendo una contracorriente de alta tensión que destruiría el [[transistor_bjt_corte_activa_saturacion]] o el pin de [[arquitectura_arduino_y_pines]]. Para absorber este pico se conecta un diodo estándar (ej. 1N4007) en antiparalelo con la bobina.

---

## ¿Por qué importa?
1. **Aislamiento Galvánico**: Protege al usuario y a los microcontroladores de baja tensión de los peligros de la red eléctrica de $230\text{ V}$.
2. **Control de cargas pesadas**: Permite que un pequeño pin de Arduino que entrega solo $5\text{ V}$ y $20\text{ mA}$ encienda un motor industrial de $2\text{ kW}$, una bomba de agua o un radiador.

---

## ¿Cómo se aplica o relaciona?
* Controlado mediante transistores en [[transistor_bjt_corte_activa_saturacion]].
* Utilizado en automatismos y prácticas de taller en [[fuente_06_taller_y_proyectos_practicos]].
