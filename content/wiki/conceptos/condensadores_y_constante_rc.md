---
title: Condensadores y Circuito Temporizador RC
tags: [condensadores, temporizacion, circuitos, 1a_evaluacion, 4eso]
aliases: [Condensador, Capacidad, Constante RC, Circuito RC]
---

# Condensadores y Circuito Temporizador RC

## ¿Qué es?
Un **condensador** o capacitor es un componente pasivo capaz de almacenar energía eléctrica en forma de campo electrostático entre dos placas conductoras (armaduras) separadas por un material aislante (dieléctrico).

### Magnitudes y Ecuación Fundamental:
$$Q = C \cdot V$$

Donde:
* **$Q$**: Carga eléctrica almacenada en **Culombios (C)**.
* **$C$**: Capacidad eléctrica en **Faradios (F)**. En la práctica se usan submúltiplos:
  * Microfaradio: $1\,\mu\text{F} = 10^{-6}\text{ F}$
  * Nanofaradio: $1\text{ nF} = 10^{-9}\text{ F} = 0{,}001\,\mu\text{F}$
  * Picofaradio: $1\text{ pF} = 10^{-12}\text{ F}$
* **$V$**: Diferencia de potencial entre armaduras (V).

### Asociación de Condensadores:
* **Paralelo**: Las capacidades se suman directamente:
  $$C_{eq} = C_1 + C_2 + C_3 + \dots$$
* **Serie**: La inversa de la capacidad equivalente es la suma de inversas:
  $$\frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2} + \dots \quad \Rightarrow \quad C_{eq} = \frac{C_1 \cdot C_2}{C_1 + C_2}$$

### Circuito RC y Constante de Tiempo ($\tau$):
Al conectar una resistencia $R$ y un condensador $C$ en serie con una fuente $V_{cc}$, la carga no es instantánea:

$$\tau = R \cdot C \quad [\text{segundos}]$$

* **Curva de Carga**: $V_c(t) = V_{cc} \left(1 - e^{-t/\tau}\right)$
  * En $t = 1\tau$: El condensador alcanza el **$63{,}2\%$** de $V_{cc}$.
  * En $t = 5\tau$: Se considera **completamente cargado** ($99{,}3\% \approx 100\%$).
* **Curva de Descarga**: $V_c(t) = V_0 \cdot e^{-t/\tau}$
  * En $t = 1\tau$: Queda el $36{,}8\%$ del voltaje inicial.
  * En $t = 5\tau$: Totalmente descargado.

---

## ¿Por qué importa?
1. **Temporización analógica**: La constante de tiempo $\tau$ permite crear retardos de tiempo sin necesidad de software ni microcontroladores.
2. **Filtrado de fuentes de alimentación**: Convierte la corriente alterna rectificada con diodos en corriente continua suave y estable eliminando el rizado.
3. **Corazón del temporizador 555**: El comportamiento de carga y descarga del par RC es la base de oscilación en [[circuito_integrado_555_monoestable_astable]].

---

## ¿Cómo se aplica o relaciona?
* Complementa los cálculos con [[ley_de_ohm_y_potencia]].
* Práctica guiada de temporizadores con transistores en [[guia_resolucion_circuitos_electricos]].

### Ejemplo de Examen:
Circuito con $R_1 = 5\text{ k}\Omega$, $R_2 = 10\text{ k}\Omega$ en serie, y dos condensadores $C_1 = 5\,\mu\text{F}$, $C_2 = 2000\text{ nF}$ en paralelo alimentados a $12\text{ V}$:
1. **Resistencia equivalente**: $R_{eq} = R_1 + R_2 = 5000 + 10000 = 15000\,\Omega = 15\text{ k}\Omega$.
2. **Capacidad equivalente**: $C_2 = 2000\text{ nF} = 2\,\mu\text{F} \Rightarrow C_{eq} = C_1 + C_2 = 5 + 2 = 7\,\mu\text{F} = 7 \cdot 10^{-6}\text{ F}$.
3. **Constante de tiempo $\tau$**: $\tau = R_{eq} \cdot C_{eq} = 15000\,\Omega \cdot 7 \cdot 10^{-6}\text{ F} = 0{,}105\text{ s}$.
4. **Tiempo de carga completa**: $t_{\text{carga}} = 5\tau = 5 \cdot 0{,}105\text{ s} = 0{,}525\text{ s}$.
