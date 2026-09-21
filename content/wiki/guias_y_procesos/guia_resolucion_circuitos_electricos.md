---
title: Guía Metodológica de Resolución de Circuitos Eléctricos Mixtos
tags: [guia, circuitos, ejercicios, 1a_evaluacion, 4eso]
aliases: [Resolución de Circuitos, Método de Nodos y Ramas]
---

# Guía Metodológica de Resolución de Circuitos Eléctricos Mixtos

Esta guía detalla el procedimiento estándar para resolver cualquier circuito mixto de corriente continua en 4º de ESO.

---

## Procedimiento Paso a Paso

### Paso 1: Identificación y Etiquetado
1. Dibuja claramente el esquema eléctrico original.
2. Identifica la fuente de alimentación ($V_{cc}$) y numera cada resistencia ($R_1, R_2, R_3, \dots$) con sus valores y unidades en Ohmios ($\Omega$).
3. Identifica los **nodos principales** (puntos donde convergen 3 o más conductores).

### Paso 2: Reducción Progresiva a la Resistencia Equivalente ($R_{eq}$)
* Busca parejas o ramas que estén en **serie pura** (sin derivaciones intermedias) y súmalas:
  $$R_{s} = R_a + R_b$$
* Busca ramas que compartan exactamente los dos mismos nodos extremos (**paralelo puro**) y calcúlalas:
  $$R_{p} = \frac{R_a \cdot R_b}{R_a + R_b}$$
* Redibuja el circuito simplificado en cada paso hasta obtener una única resistencia equivalente total conectada a la fuente ($R_{eq}$).

### Paso 3: Cálculo de la Intensidad Total ($I_t$)
Aplica la [[ley_de_ohm_y_potencia]] sobre el circuito reducido final:

$$I_t = \frac{V_{cc}}{R_{eq}}$$

### Paso 4: Despliegue hacia atrás (Cálculo de Tensiones e Intensidades Parciales)
Retrocede paso a paso en los circuitos intermedios dibujados:
* Para elementos o bloques en **serie**: La intensidad que los atraviesa es la misma que la del bloque; calcula la caída de tensión en cada uno mediante $V_x = I_{\text{bloque}} \cdot R_x$.
* Para elementos o bloques en **paralelo**: La tensión en sus bornes es idéntica a la del bloque; calcula la intensidad por cada rama mediante $I_x = \frac{V_{\text{bloque}}}{R_x}$.

### Paso 5: Comprobación y Balance de Potencias
1. **Ley de Kirchhoff de Intensidades (1ª Ley)**: La suma de corrientes que entran a un nodo debe ser igual a la suma de las que salen.
2. **Balance de Potencia Total**: La potencia entregada por la fuente debe ser igual a la suma de potencias disipadas en cada resistencia:
   $$P_{\text{fuente}} = V_{cc} \cdot I_t \quad = \quad \sum_{i} I_i^2 \cdot R_i$$

---

## Ejemplo Completo Resuelto

```text
       +-------[ R1 = 10 Ω ]-------+
       |                           |
  (+)  |           +---[ R2 = 30 Ω ]---+
 [ 24V ]           |                   |
  (-)  |           +---[ R3 = 60 Ω ]---+
       |                               |
       +-------------------------------+
```

1. **Paralelo de $R_2$ y $R_3$**:
   $$R_{23} = \frac{30 \cdot 60}{30 + 60} = \frac{1800}{90} = 20\,\Omega$$
2. **Serie de $R_1$ y $R_{23}$**:
   $$R_{eq} = R_1 + R_{23} = 10 + 20 = 30\,\Omega$$
3. **Intensidad Total**:
   $$I_t = \frac{V}{R_{eq}} = \frac{24\text{ V}}{30\,\Omega} = 0{,}8\text{ A} = 800\text{ mA}$$
4. **Tensiones parciales**:
   * En $R_1$: $V_1 = I_t \cdot R_1 = 0{,}8\text{ A} \cdot 10\,\Omega = 8\text{ V}$.
   * En el bloque paralelo: $V_{23} = I_t \cdot R_{23} = 0{,}8\text{ A} \cdot 20\,\Omega = 16\text{ V}$. *(Comprobación: $8\text{ V} + 16\text{ V} = 24\text{ V}$)*.
5. **Corrientes de rama**:
   * En $R_2$: $I_2 = \frac{V_{23}}{R_2} = \frac{16\text{ V}}{30\,\Omega} = 0{,}533\text{ A}$.
   * En $R_3$: $I_3 = \frac{V_{23}}{R_3} = \frac{16\text{ V}}{60\,\Omega} = 0{,}267\text{ A}$. *(Comprobación: $0{,}533 + 0{,}267 = 0{,}800\text{ A}$)*.

---
*Conceptos relacionados: [[asociacion_resistencias]], [[ley_de_ohm_y_potencia]], [[codigo_colores_resistencias]].*
