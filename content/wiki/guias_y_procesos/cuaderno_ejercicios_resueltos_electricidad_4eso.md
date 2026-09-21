---
title: Cuaderno de Ejercicios Resueltos de Electricidad y Circuitos (4º ESO)
tags: [ejercicios, electricidad, ley_de_ohm, resistencias, serie_paralelo, 1a_evaluacion, 4eso]
aliases: [Ejercicios Electricidad 4ESO, Solucionario Electricidad 4ESO]
---

# Cuaderno de Ejercicios Resueltos de Electricidad y Circuitos (4º ESO)

Material didáctico estructurado en fichas de trabajo con enunciados, recordatorios teóricos clave y soluciones detalladas paso a paso.

---

## Ficha 1: Aplicación Práctica de la Ley de Ohm

> [!NOTE]
> **Recordatorio Clave**:
> * $V = I \cdot R \quad ; \quad I = \frac{V}{R} \quad ; \quad R = \frac{V}{I}$
> * **Unidades**: Tensión $V$ en Voltios ($\text{V}$), Corriente $I$ en Amperios ($\text{A}$), Resistencia $R$ en Ohmios ($\Omega$).
> * **Factores de conversión**: $1\text{ mA} = 10^{-3}\text{ A} = 0{,}001\text{ A}$ ; $1\text{ k}\Omega = 1000\,\Omega$.

### Ejercicio 1
Una bombilla incandescente está conectada a una pila de $9\text{ V}$. Si el filamento tiene una resistencia interna de $45\,\Omega$, calcula la intensidad de corriente eléctrica que circula por la bombilla.
* **Fórmula**: $I = \frac{V}{R}$
* **Sustitución**: $I = \frac{9\text{ V}}{45\,\Omega} = 0{,}2\text{ A}$
* **Resultado**: **$I = 0{,}2\text{ A} = 200\text{ mA}$**.

### Ejercicio 2
Por el motor eléctrico de un taladro conectado a la red doméstica de $230\text{ V}$ se mide una corriente de $2{,}5\text{ A}$. Determina el valor de la resistencia eléctrica que opone dicho motor.
* **Fórmula**: $R = \frac{V}{I}$
* **Sustitución**: $R = \frac{230\text{ V}}{2{,}5\text{ A}} = 92\,\Omega$
* **Resultado**: **$R = 92\,\Omega$**.

### Ejercicio 3
Un radiador eléctrico tiene una resistencia de $28\,\Omega$. Si al encenderlo circula por él una intensidad de $8\text{ A}$, ¿a qué diferencia de potencial (voltaje) está conectado?
* **Fórmula**: $V = I \cdot R$
* **Sustitución**: $V = 8\text{ A} \cdot 28\,\Omega = 224\text{ V}$
* **Resultado**: **$V = 224\text{ V}$**.

### Ejercicio 4
Un diodo LED de alta luminosidad funciona con un voltaje de $3\text{ V}$ y absorbe una corriente máxima de $20\text{ mA}$. Calcula la resistencia interna que presenta. (Convierte previamente los miliamperios a amperios).
* **Conversión**: $I = 20\text{ mA} = \frac{20}{1000}\text{ A} = 0{,}02\text{ A}$
* **Fórmula**: $R = \frac{V}{I} = \frac{3\text{ V}}{0{,}02\text{ A}} = 150\,\Omega$
* **Resultado**: **$R = 150\,\Omega$**.

---

## Ficha 2: Asociación de Resistencias en Serie

> [!NOTE]
> **Recordatorio Clave**:
> * Resistencia equivalente: $R_{eq} = R_1 + R_2 + \dots + R_n$.
> * La **intensidad de corriente es idéntica** en todos los elementos ($I_t = I_1 = I_2 = \dots$).
> * La **tensión total se reparte**: $V_t = V_1 + V_2 + \dots$

### Ejercicio 1
Dos resistencias de $R_1 = 30\,\Omega$ y $R_2 = 50\,\Omega$ se conectan en serie a los bornes de un generador de $12\text{ V}$.
* **a) Esquema del circuito**: Fuente de $12\text{ V}$ en serie con $R_1$ y $R_2$.
* **b) Resistencia equivalente e intensidad total**:
  $$R_{eq} = R_1 + R_2 = 30\,\Omega + 50\,\Omega = 80\,\Omega$$
  $$I_t = \frac{V}{R_{eq}} = \frac{12\text{ V}}{80\,\Omega} = 0{,}15\text{ A} = 150\text{ mA}$$
* **Resultado**: **$R_{eq} = 80\,\Omega$** ; **$I_t = 0{,}15\text{ A}$**.

### Ejercicio 2
Se montan en serie tres resistencias cuyos valores son: $R_1 = 120\,\Omega$, $R_2 = 250\,\Omega$ y $R_3 = 130\,\Omega$.
* **a) Esquema**: Conexión lineal sucesiva de las 3 resistencias.
* **b) Resistencia equivalente total**:
  $$R_{eq} = R_1 + R_2 + R_3 = 120 + 250 + 130 = 500\,\Omega = 0{,}5\text{ k}\Omega$$
* **Resultado**: **$R_{eq} = 500\,\Omega$**.

### Ejercicio 3
Una tira luminosa decorativa está formada por tres lámparas conectadas en serie con resistencias de $R_1 = 15\,\Omega$, $R_2 = 25\,\Omega$ y $R_3 = 40\,\Omega$, alimentadas a $24\text{ V}$.
* **a) Esquema**: Cadena serie de las tres lámparas.
* **b) Resistencia equivalente y corriente**:
  $$R_{eq} = 15 + 25 + 40 = 80\,\Omega$$
  $$I = \frac{24\text{ V}}{80\,\Omega} = 0{,}3\text{ A} = 300\text{ mA}$$
* **Resultado**: **$R_{eq} = 80\,\Omega$** ; **$I = 0{,}3\text{ A}$** (circula la misma corriente por las tres bombillas).

---

## Ficha 3: Asociación de Resistencias en Paralelo

> [!NOTE]
> **Recordatorio Clave**:
> * Fórmula general: $\frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2} + \dots + \frac{1}{R_n}$.
> * Para 2 resistencias: $R_{eq} = \frac{R_1 \cdot R_2}{R_1 + R_2}$.
> * Para $N$ resistencias idénticas: $R_{eq} = \frac{R}{N}$.
> * Todas las ramas soportan el **mismo voltaje** ($V_t = V_1 = V_2$). La corriente total se divide: $I_t = I_1 + I_2$.
> * **Propiedad física**: $R_{eq}$ siempre es **menor que la menor** de las resistencias asociadas.

### Ejercicio 1
Se conectan dos resistencias de $R_1 = 20\,\Omega$ y $R_2 = 30\,\Omega$ en paralelo a una batería de $12\text{ V}$.
* **a) Esquema**: Circuito de dos ramas con nodos de unión superior e inferior.
* **b) Resistencia equivalente**:
  $$R_{eq} = \frac{R_1 \cdot R_2}{R_1 + R_2} = \frac{20 \cdot 30}{20 + 30} = \frac{600}{50} = 12\,\Omega$$
* **Resultado**: **$R_{eq} = 12\,\Omega$** *(Comprobación: $12\,\Omega < 20\,\Omega$)*.

### Ejercicio 2
Dos altavoces pasivos de sonido con idéntica resistencia de $R_1 = 8\,\Omega$ y $R_2 = 8\,\Omega$ se asocian en paralelo a la salida de un amplificador de audio.
* **a) Esquema**: Dos altavoces en paralelo compartiendo bornes.
* **b) Resistencia equivalente**:
  $$R_{eq} = \frac{R}{N} = \frac{8\,\Omega}{2} = 4\,\Omega \quad \left(\text{o } \frac{8 \cdot 8}{8 + 8} = \frac{64}{16} = 4\,\Omega\right)$$
* **Resultado**: **$R_{eq} = 4\,\Omega$**.

### Ejercicio 3
En un circuito se disponen en paralelo tres resistencias: $R_1 = 60\,\Omega$, $R_2 = 30\,\Omega$ y $R_3 = 20\,\Omega$, alimentadas por una fuente de $18\text{ V}$.
* **a) Esquema**: Tres ramas paralelas con nodos comunes.
* **b) Resistencia equivalente e intensidad total**:
  $$\frac{1}{R_{eq}} = \frac{1}{60} + \frac{1}{30} + \frac{1}{20} = \frac{1 + 2 + 3}{60} = \frac{6}{60} = \frac{1}{10} \quad \Longrightarrow \quad R_{eq} = 10\,\Omega$$
  $$I_t = \frac{V}{R_{eq}} = \frac{18\text{ V}}{10\,\Omega} = 1{,}8\text{ A}$$
* **Resultado**: **$R_{eq} = 10\,\Omega$** ; **$I_t = 1{,}8\text{ A}$**.

---
*Conceptos relacionados: [[ley_de_ohm_y_potencia]], [[asociacion_resistencias]], [[guia_resolucion_circuitos_electricos]].*
