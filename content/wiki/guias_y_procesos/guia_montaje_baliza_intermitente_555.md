---
title: Guía de Construcción: Baliza Intermitente de Dos Luces con CI 555
tags: [guia, ci_555, baliza, taller, proyecto_electronica, 4eso]
aliases: [Baliza 555, Proyecto Baliza, Intermitente 555]
---

# Guía de Construcción: Baliza Intermitente de Dos Luces con CI 555

## 1. Descripción del Proyecto
La **baliza intermitente** es un circuito clásico de señalización de emergencia que hace destellar de forma alterna dos diodos LED (o un grupo de LEDs) a una frecuencia calibrada mediante el temporizador **NE555 configurado en modo astable**.

![Esquema de la Baliza Intermitente con 555](file:///Users/luis/Documents/Espacio%20antigr%C3%A1vity/TECNOLOGIA4%C2%BA/wiki/assets/baliza_intermitente_555.png)

---

## 2. Lista de Componentes Necesarios:
* $1$ Circuito Integrado **NE555**.
* $1$ Zócalo DIP-8 para circuito integrado.
* $1$ Resistencia $R_1 = 1\text{ k}\Omega$ ($1/4\text{ W}$).
* $1$ Potenciómetro o resistencia $R_2 = 100\text{ k}\Omega$ (permite regular la velocidad del destello).
* $1$ Condensador electrolítico $C_1 = 10\,\mu\text{F} / 25\text{V}$.
* $1$ Condensador cerámico $C_2 = 10\text{ nF}$ (desacoplo pin 5).
* $2$ Diodos LED (uno rojo y uno verde o ámbar).
* $2$ Resistencias de protección para LED $R_3, R_4 = 470\,\Omega$.
* $1$ Portapilas de $9\text{ V}$ con broche.
* Placa protoboard o placa de circuito impreso para soldar.

---

## 3. Principio de Funcionamiento de la Alternancia de LEDs
La patilla 3 (salida) del 555 conmuta entre $+V_{cc}$ y $0\text{ V}$:
1. **Cuando la salida (pin 3) está en nivel ALTO ($+V_{cc}$)**:
   * El LED conectado entre pin 3 y GND se polariza directamente y **se enciende**.
   * El LED conectado entre Vcc y pin 3 queda sin diferencia de potencial y **se apaga**.
2. **Cuando la salida (pin 3) está en nivel BAJO ($0\text{ V}$)**:
   * El LED conectado a GND **se apaga**.
   * El LED conectado a Vcc se polariza directamente hacia el pin 3 y **se enciende**.

---

## 4. Fórmulas de Calibración
$$T_H = 0{,}693 \cdot (R_1 + R_2) \cdot C_1$$
$$T_L = 0{,}693 \cdot R_2 \cdot C_1$$
$$f = \frac{1{,}44}{(R_1 + 2R_2) \cdot C_1}$$

---
*Conceptos relacionados: [[circuito_integrado_555_monoestable_astable]], [[diodos_y_leds]], [[guia_montaje_y_calculo_timer_555]].*
