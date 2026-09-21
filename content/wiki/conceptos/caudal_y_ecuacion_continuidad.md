---
title: Caudal y Ecuación de Continuidad en Tuberías
tags: [neumatica, hidraulica, fluidos, caudal, 3a_evaluacion, 4eso]
aliases: [Caudal, Ecuación de Continuidad, Velocidad de Fluidos]
---

# Caudal y Ecuación de Continuidad en Tuberías

## ¿Qué es?
En el estudio de fluidos en régimen estacionario e incompresible que circulan por una conducción cerrada (tubería):

### 1. Caudal Volumétrico ($Q$)
Es el volumen de fluido ($V$) que atraviesa una sección transversal de la tubería por unidad de tiempo ($t$):

$$Q = \frac{V}{t} = \frac{S \cdot L}{t} = S \cdot v$$

Donde:
* **$Q$**: Caudal en **$\text{m}^3/\text{s}$** (o en litros/minuto: $1\text{ litro} = 1\text{ dm}^3 = 10^{-3}\text{ m}^3$, $1\text{ min} = 60\text{ s} \Rightarrow 1\text{ l/min} = \frac{10^{-3}}{60}\text{ m}^3/\text{s}$).
* **$S$**: Sección de la tubería ($\text{m}^2$).
* **$v$**: Velocidad lineal de avance del fluido ($\text{m/s}$).

### 2. Ecuación de Continuidad
Por el principio de conservación de la masa, si no existen fugas ni aportes, el caudal volumétrico es **constante** a lo largo de cualquier punto de la tubería:

$$Q_1 = Q_2 \quad \Longrightarrow \quad S_1 \cdot v_1 = S_2 \cdot v_2$$

* **Consecuencia física**: Al estrecharse una tubería ($S_2 < S_1$), la velocidad del fluido **aumenta** en proporción inversa ($v_2 > v_1$).

---

## ¿Por qué importa?
1. **Dimensionamiento de conducciones**: Permite seleccionar el diámetro de mangueras y tuberías para garantizar que la velocidad del aire no cause caídas de presión excesivas ni ruido en el taller.
2. **Control de actuadores**: Determina la velocidad de avance de los vástagos de los cilindros neumáticos e hidráulicos.

---

## ¿Cómo se aplica o relaciona?
* Resolución paso a paso en [[guia_resolucion_problemas_pascal_y_continuidad]].
* Integrado en circuitos de control en [[valvulas_logicas_simultaneidad_selectora]].

### Ejemplo de Examen:
Una tubería con un caudal de $90\text{ l/min}$ se estrecha desde una sección $S_1 = 3000\text{ mm}^2$ hasta $S_2 = 8\text{ cm}^2$. Calcula la velocidad del fluido (en $\text{m/s}$) en la zona ancha y en la zona estrecha:
1. **Conversión del caudal al SI**:
   $$Q = 90\text{ l/min} = \frac{90 \cdot 10^{-3}\text{ m}^3}{60\text{ s}} = 1{,}5 \cdot 10^{-3}\text{ m}^3/\text{s}$$
2. **Conversión de secciones al SI**:
   * $S_1 = 3000\text{ mm}^2 = 3000 \cdot 10^{-6}\text{ m}^2 = 0{,}003\text{ m}^2$.
   * $S_2 = 8\text{ cm}^2 = 8 \cdot 10^{-4}\text{ m}^2 = 0{,}0008\text{ m}^2$.
3. **Velocidad en la zona ancha ($v_1$)**:
   $$v_1 = \frac{Q}{S_1} = \frac{0{,}0015\text{ m}^3/\text{s}}{0{,}003\text{ m}^2} = 0{,}5\text{ m/s}$$
4. **Velocidad en la zona estrecha ($v_2$)**:
   $$v_2 = \frac{Q}{S_2} = \frac{0{,}0015\text{ m}^3/\text{s}}{0{,}0008\text{ m}^2} = 1{,}875\text{ m/s}$$
