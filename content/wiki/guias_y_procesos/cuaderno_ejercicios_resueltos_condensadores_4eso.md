---
title: Cuaderno de Ejercicios Resueltos de Condensadores y Circuito RC (4º ESO)
tags: [ejercicios, condensadores, capacidad, conversion_unidades, circuito_rc, 1a_evaluacion, 4eso]
aliases: [Ejercicios Condensadores 4ESO, Solucionario Condensadores 4ESO]
---

# Cuaderno de Ejercicios Resueltos de Condensadores y Circuito RC (4º ESO)

Material didáctico estructurado en fichas de trabajo con enunciados, tablas de conversión, recordatorios teóricos clave y soluciones detalladas paso a paso.

---

## Ficha 1: Asociación de Condensadores en Serie

> [!NOTE]
> **Recordatorio Clave**:
> * Fórmula general: $\frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2} + \dots + \frac{1}{C_n}$.
> * Para dos condensadores: $C_{eq} = \frac{C_1 \cdot C_2}{C_1 + C_2}$.
> * Para $N$ condensadores iguales: $C_{eq} = \frac{C}{N}$.
> * **¡Atención!**: En serie, la capacidad equivalente siempre es **MENOR** que la menor de las capacidades asociadas (al aumentar la distancia efectiva entre armaduras extremas).

### Ejercicio 1
Se conectan en serie dos condensadores de capacidades $C_1 = 20\,\mu\text{F}$ y $C_2 = 30\,\mu\text{F}$.
* **a) Esquema**: Dos condensadores en la misma rama continua.
* **b) Capacidad equivalente**:
  $$C_{eq} = \frac{C_1 \cdot C_2}{C_1 + C_2} = \frac{20 \cdot 30}{20 + 30} = \frac{600}{50} = 12\,\mu\text{F}$$
* **Resultado**: **$C_{eq} = 12\,\mu\text{F}$**.

### Ejercicio 2
Dos condensadores idénticos de $C_1 = 100\,\mu\text{F}$ y $C_2 = 100\,\mu\text{F}$ se asocian en serie.
* **a) Esquema**: Asociación en serie de dos condensadores iguales.
* **b) Capacidad equivalente**:
  $$C_{eq} = \frac{C}{2} = \frac{100\,\mu\text{F}}{2} = 50\,\mu\text{F} \quad \left(\text{o } \frac{100 \cdot 100}{100 + 100} = \frac{10000}{200} = 50\,\mu\text{F}\right)$$
* **Resultado**: **$C_{eq} = 50\,\mu\text{F}$**.

### Ejercicio 3
En un circuito se asocian en serie tres condensadores con valores $C_1 = 12\,\mu\text{F}$, $C_2 = 6\,\mu\text{F}$ y $C_3 = 4\,\mu\text{F}$.
* **a) Esquema**: Conexión de los tres componentes alineados.
* **b) Capacidad equivalente (m.c.m.)**:
  $$\frac{1}{C_{eq}} = \frac{1}{12} + \frac{1}{6} + \frac{1}{4} = \frac{1 + 2 + 3}{12} = \frac{6}{12} = \frac{1}{2} \quad \Longrightarrow \quad C_{eq} = 2\,\mu\text{F}$$
* **Resultado**: **$C_{eq} = 2\,\mu\text{F}$**.

---

## Ficha 2: Asociación de Condensadores en Paralelo

> [!NOTE]
> **Recordatorio Clave**:
> * Fórmula: $C_{eq} = C_1 + C_2 + \dots + C_n$.
> * En paralelo, las capacidades se **SUMAN directamente** (al compartir la misma tensión, la superficie efectiva total de las placas aumenta).
> * $C_{eq}$ siempre es **MAYOR** que cualquiera individual.

### Ejercicio 1
Se montan en paralelo dos condensadores de capacidades $C_1 = 47\,\mu\text{F}$ y $C_2 = 100\,\mu\text{F}$ conectados a una pila de $9\text{ V}$.
* **a) Esquema**: Dos ramas paralelas con nodos de bifurcación.
* **b) Capacidad equivalente**:
  $$C_{eq} = C_1 + C_2 = 47\,\mu\text{F} + 100\,\mu\text{F} = 147\,\mu\text{F}$$
* **Resultado**: **$C_{eq} = 147\,\mu\text{F}$**.

### Ejercicio 2
Para estabilizar una fuente de tensión se conectan tres condensadores en paralelo: $C_1 = 10\,\mu\text{F}$, $C_2 = 22\,\mu\text{F}$ y $C_3 = 33\,\mu\text{F}$.
* **a) Esquema**: Tres ramas paralelas.
* **b) Capacidad total**:
  $$C_{eq} = C_1 + C_2 + C_3 = 10 + 22 + 33 = 65\,\mu\text{F}$$
* **Resultado**: **$C_{eq} = 65\,\mu\text{F}$**.

### Ejercicio 3
Un técnico necesita obtener una capacidad total equivalente de exactamente $500\text{ nF}$ y dispone de un condensador $C_1 = 320\text{ nF}$.
* **a) Conexión**: Se debe asociar un segundo condensador $C_2$ en **paralelo** para que sume capacidad.
* **b) Cálculo de $C_2$**:
  $$C_{eq} = C_1 + C_2 \quad \Longrightarrow \quad C_2 = C_{eq} - C_1 = 500\text{ nF} - 320\text{ nF} = 180\text{ nF}$$
* **Resultado**: **$C_2 = 180\text{ nF}$**.

---

## Ficha 3: Conversión de Unidades de Capacidad Eléctrica

> [!NOTE]
> **Tabla de Equivalencias**:
> $$1\text{ Faradio (F)} = 10^3\text{ mF} = 10^6\,\mu\text{F} = 10^9\text{ nF} = 10^{12}\text{ pF}$$
> * Para pasar a una unidad más pequeña (hacia la derecha $\rightarrow$): **multiplicar por $10^3$ ($1000$)**.
> * Para pasar a una unidad más grande (hacia la izquierda $\leftarrow$): **dividir entre $10^3$ ($1000$)**.

### Tabla 1: Operaciones de Conversión Directa

| Nº | Valor Inicial | Unidad Destino | Operación | Resultado Final |
| :---: | :---: | :---: | :---: | :---: |
| 1 | $4{,}7\,\mu\text{F}$ | Nanofaradios ($\text{nF}$) | $4{,}7 \times 10^3\text{ nF}$ | **$4700\text{ nF}$** |
| 2 | $220\text{ nF}$ | Microfaradios ($\mu\text{F}$) | $220 / 10^3\,\mu\text{F}$ | **$0{,}22\,\mu\text{F}$** |
| 3 | $100.000\text{ pF}$ | Nanofaradios ($\text{nF}$) | $100000 / 10^3\text{ nF}$ | **$100\text{ nF}$** |
| 4 | $33\text{ nF}$ | Picofaradios ($\text{pF}$) | $33 \times 10^3\text{ pF}$ | **$33000\text{ pF}$** |
| 5 | $470\,\mu\text{F}$ | Faradios ($\text{F}$) | $470 \times 10^{-6}\text{ F}$ | **$4{,}7 \times 10^{-4}\text{ F}$ ($0{,}00047\text{ F}$)** |

### Tabla 2: Mismo Valor en Cuatro Unidades

| Condensador | Faradios ($	ext{F}$) | Microfaradios ($\mu	ext{F}$) | Nanofaradios ($	ext{nF}$) | Picofaradios ($	ext{pF}$) |
| :--- | :---: | :---: | :---: | :---: |
| **Condensador A** | $10^{-5}	ext{ F}$ | **$10\,\mu	ext{F}$** | $10.000	ext{ nF}$ | $10.000.000	ext{ pF}$ ($10^7	ext{ pF}$) |
| **Condensador B** | $10^{-8}	ext{ F}$ | $0{,}01\,\mu	ext{F}$ | **$10	ext{ nF}$** | $10.000	ext{ pF}$ ($10^4	ext{ pF}$) |
| **Condensador C** | $10^{-10}	ext{ F}$ | $0{,}0001\,\mu	ext{F}$ ($10^{-4}\,\mu	ext{F}$) | $0{,}1	ext{ nF}$ | **$100	ext{ pF}$** |

---

## Ficha 4: Tiempo de Carga y Descarga con Condensadores en Serie (Circuito RC)

> [!NOTE]
> **Fórmulas Fundamentales**:
> 1. Constante de tiempo: $\tau = R \cdot C_{eq}$ (con $R$ en $\Omega$ y $C$ en Faradios $\text{F}$, $\tau$ resulta en segundos $\text{s}$).
> 2. Carga al $63{,}2\%$ del voltaje máximo: $t = 1\tau$.
> 3. Carga o descarga completa ($99{,}3\% \approx 100\%$): $t_{\text{total}} \approx 5\tau = 5 \cdot R \cdot C_{eq}$.

### Ejercicio 1
En un temporizador de una luz de cortesía se conectan en serie dos condensadores de $C_1 = 200\,\mu\text{F}$ y $C_2 = 300\,\mu\text{F}$, junto con una resistencia $R = 10\text{ k}\Omega$ ($10000\,\Omega$) conectada a un generador.
* **a) Capacidad equivalente**:
  $$C_{eq} = \frac{200 \cdot 300}{200 + 300} = \frac{60000}{500} = 120\,\mu\text{F} = 120 \times 10^{-6}\text{ F} = 0{,}00012\text{ F}$$
* **b) Constante de tiempo $\tau$ y tiempo total de carga**:
  $$\tau = R \cdot C_{eq} = 10000\,\Omega \times 120 \times 10^{-6}\text{ F} = 1{,}2\text{ s}$$
  $$t_{\text{carga total}} = 5 \cdot \tau = 5 \times 1{,}2\text{ s} = 6\text{ s}$$
* **Resultado**: **$\tau = 1{,}2\text{ s}$** ; **$t_{\text{total}} = 6\text{ s}$**.

### Ejercicio 2
Un circuito oscilador dispone de dos condensadores en serie de $C_1 = 10\,\mu\text{F}$ y $C_2 = 40\,\mu\text{F}$, conectados a una resistencia $R = 250\text{ k}\Omega$ ($250000\,\Omega$).
* **a) Esquema**: Circuito RC serie completo con generador, interruptor, $R$ y los dos condensadores $C_1, C_2$.
* **b) Capacidad equivalente y tiempo de descarga total**:
  $$C_{eq} = \frac{10 \cdot 40}{10 + 40} = \frac{400}{50} = 8\,\mu\text{F} = 8 \times 10^{-6}\text{ F}$$
  $$\tau = R \cdot C_{eq} = 250000\,\Omega \times 8 \times 10^{-6}\text{ F} = 2\text{ s}$$
  $$t_{\text{descarga total}} = 5\tau = 5 \times 2\text{ s} = 10\text{ s}$$
* **Resultado**: **$C_{eq} = 8\,\mu\text{F}$** ; **$t_{\text{descarga}} = 10\text{ s}$**.

### Ejercicio 3
Se unen en serie dos condensadores idénticos de $C_1 = 50\,\mu\text{F}$ y $C_2 = 50\,\mu\text{F}$ en serie con una resistencia $R = 40\text{ k}\Omega$ ($40000\,\Omega$).
* **a) Capacidad equivalente**:
  $$C_{eq} = \frac{50}{2} = 25\,\mu\text{F} = 25 \times 10^{-6}\text{ F}$$
* **b) Constante de tiempo $\tau$ y tiempo al 63% de carga**:
  $$\tau = R \cdot C_{eq} = 40000\,\Omega \times 25 \times 10^{-6}\text{ F} = 1\text{ s}$$
  * El circuito alcanza el $63{,}2\%$ de carga exactamente al transcurrir **$t = 1\tau = 1\text{ segundo}$** (y la carga completa en $5\tau = 5\text{ segundos}$).
* **Resultado**: **$C_{eq} = 25\,\mu\text{F}$** ; **$\tau = 1\text{ s}$** ; **$t_{63\%} = 1\text{ s}$**.

---
*Conceptos relacionados: [[condensadores_y_constante_rc]], [[ley_de_ohm_y_potencia]], [[guia_resolucion_circuitos_electricos]].*
