---
title: Neumática e Hidráulica (Fuerza, Presión y Principio de Pascal)
tags: [neumatica, hidraulica, pascal, presion, 3a_evaluacion, 4eso]
aliases: [Presión, Principio de Pascal, Prensa Hidráulica, Neumática Básica]
---

# Neumática e Hidráulica (Fuerza, Presión y Principio de Pascal)

## ¿Qué es?
La **Neumática** emplea **aire comprimido** (fluido compresible) como medio para transmitir energía y realizar trabajo mecánico, mientras que la **Hidráulica** emplea **líquidos/aceites** (fluidos prácticamente incompresibles).

### Conceptos Físicos Fundamentales:

#### 1. Presión ($P$)
La presión es la relación entre la fuerza perpendicular ($F$) aplicada y la superficie o sección ($S$) sobre la que actúa:

$$P = \frac{F}{S}$$

* **Unidades en el SI**:
  * Fuerza ($F$): **Newtons (N)** (Recordatorio: $P_{\text{peso}} = m \cdot g \approx m \cdot 10\text{ m/s}^2$).
  * Superficie ($S$): **Metros cuadrados ($\text{m}^2$)**.
  * Presión ($P$): **Pascales (Pa)** ($1\text{ Pa} = 1\text{ N/m}^2$).
* **Unidades Técnicas e Industriales**:
  * **Bar**: $1\text{ bar} = 10^5\text{ Pa} = 100\text{ kPa} \approx 1\text{ kg/cm}^2 \approx 1\text{ atmósfera}$.

#### 2. Principio de Pascal
Enunciado por Blaise Pascal: *"La presión ejercida sobre un fluido incompresible en equilibrio dentro de un recipiente de paredes indeformables se transmite con igual intensidad en todas las direcciones y en todos los puntos del fluido"*.

### La Prensa Hidráulica:
Dado que la presión en ambos émbolos es idéntica ($P_1 = P_2$):

$$\frac{F_1}{S_1} = \frac{F_2}{S_2} \quad \Longrightarrow \quad F_2 = F_1 \cdot \frac{S_2}{S_1}$$

Como $S = \pi \cdot r^2 = \pi \cdot \left(\frac{d}{2}\right)^2$:

$$\frac{F_1}{d_1^2} = \frac{F_2}{d_2^2}$$

* **Efecto Multiplicador**: Si el émbolo grande tiene una superficie $100$ veces mayor que el émbolo pequeño, la fuerza generada en la salida ($F_2$) será $100$ veces superior a la fuerza aplicada en la entrada ($F_1$).

---

## ¿Por qué importa?
1. **Multiplicación de fuerza**: Permite levantar camiones o hipopótamos con el esfuerzo de un pie humano mediante gatos hidráulicos y frenos de disco en vehículos.
2. **Rapidez y limpieza de la neumática**: Ideal para líneas de fabricación automatizada, robots de envasado y puertas de autobuses.

---

## ¿Cómo se aplica o relaciona?
* Consulta la guía de ejercicios resueltos en [[guia_resolucion_problemas_pascal_y_continuidad]].
* Continuación con la dinámica de fluidos en [[caudal_y_ecuacion_continuidad]].
* Elementos del circuito en [[circuito_neumatico_frl_compresor]].

### Ejemplo de Examen (Problema del Hipopótamo):
Un hipopótamo de masa $1800\text{ kg}$ ($F_2 = 18000\text{ N}$) está situado sobre el émbolo grande de $d_2 = 2\text{ m}$ ($r_2 = 1\text{ m}$). El émbolo pequeño tiene diámetro $d_1 = 18\text{ cm} = 0{,}18\text{ m}$ ($r_1 = 0{,}09\text{ m}$). ¿Qué fuerza $F_1$ hay que aplicar?
1. **Superficie 1**: $S_1 = \pi \cdot (0{,}09)^2 = 0{,}02545\text{ m}^2$.
2. **Superficie 2**: $S_2 = \pi \cdot (1)^2 = 3{,}1416\text{ m}^2$.
3. **Cálculo de la fuerza $F_1$**:
   $$F_1 = F_2 \cdot \frac{S_1}{S_2} = 18000 \cdot \frac{0{,}02545}{3{,}1416} = 18000 \cdot \left(\frac{0{,}18}{2}\right)^2 = 18000 \cdot (0{,}09)^2 = 18000 \cdot 0{,}0081 = 145{,}8\text{ N}$$
*(¡Una pequeña fuerza de apenas $14{,}6\text{ kg}$ permite elevar al animal de $1{,}8$ toneladas!)*.
