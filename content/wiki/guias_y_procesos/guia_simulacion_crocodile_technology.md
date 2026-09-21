---
title: Guía de Simulación con Crocodile Clips y Crocodile Technology
tags: [guia, software, simulacion, crocodile, 1a_evaluacion, 2a_evaluacion, 4eso]
aliases: [Simulador Crocodile, Crocodile Technology, Prácticas Crocodile]
---

# Guía de Simulación con Crocodile Clips y Crocodile Technology

## 1. Introducción y Entorno de Trabajo
**Crocodile Technology (Yenka)** es el software de simulación estándar para Tecnología de 4º de ESO. Permite simular circuitos eléctricos, analógicos, puertas lógicas y sistemas mecánicos de forma visual e interactiva sin riesgo de quemar componentes.

---

## 2. Bibliotecas de Componentes Principales

### A. Electricidad y Electrónica Analógica
* **Fuentes de alimentación**: Pilas, baterías ajustables de CC, generadores de señal.
* **Componentes pasivos**: Resistencias (editables en $\Omega, \text{k}\Omega, \text{M}\Omega$), condensadores, potenciómetros, fotorresistencias LDR, termistores.
* **Semiconductores**: Diodos estándar, diodos LED (seleccionables por color), transistores NPN (ej. 2N3904, BC547) y PNP.
* **Instrumentos de medida**: Voltímetros, amperímetros, osciloscopios virtuales en tiempo real.

### B. Electrónica Digital
* **Entradas lógicas**: Interruptores SPST, pulsadores, generadores de niveles lógicos constantes '0' y '1'.
* **Puertas lógicas**: NOT, AND, OR, NAND, NOR, XOR de 2, 3 y 4 entradas.
* **Salidas lógicas**: Puntas lógicas indicadoras de estado (verde = 0, rojo = 1), visualizadores de 7 segmentos.

---

## 3. Buenas Prácticas de Simulación
1. **Evitar cortocircuitos**: El software simula la destrucción y explosión de componentes si se sobrepasa la potencia máxima o la corriente de un LED.
2. **Uso de tierras (GND)**: Conectar siempre la referencia de masa en circuitos analógicos complejos y temporizadores 555.
3. **Comprobación de tablas de verdad**: Utilizar interruptores dobles o cuádruples para recorrer metódicamente las combinaciones de entradas binarias ($0000$ a $1111$).

---
*Conceptos relacionados: [[puertas_logicas_fundamentales]], [[mapas_de_karnaugh]], [[diodos_y_leds]], [[transistor_bjt_corte_activa_saturacion]].*
