---
title: Ley de Ohm y Potencia Eléctrica
tags: [electricidad, fisica, circuitos, 1a_evaluacion, 4eso]
aliases: [Ley de Ohm, Potencia Eléctrica, Efecto Joule]
---

# Ley de Ohm y Potencia Eléctrica

## ¿Qué es?
La **Ley de Ohm** es la relación matemática fundamental que rige el comportamiento de los circuitos eléctricos en corriente continua. Establece que la diferencia de potencial o tensión ($V$) aplicada entre los extremos de un conductor es directamente proporcional a la intensidad de corriente ($I$) que circula por él, siendo la constante de proporcionalidad la resistencia eléctrica ($R$) del elemento:

$$V = I \cdot R$$

Donde:
* **$V$**: Tensión, voltaje o diferencia de potencial, medida en **Voltios (V)**.
* **$I$**: Intensidad de corriente eléctrica, medida en **Amperios (A)** (frecuentemente en miliamperios, $1\text{ mA} = 10^{-3}\text{ A}$).
* **$R$**: Resistencia eléctrica, medida en **Ohmios ($\Omega$)** (o kiloohmios, $1\text{ k}\Omega = 10^3\,\Omega$).

La **Potencia Eléctrica ($P$)** representa la cantidad de energía eléctrica transferida o transformada por unidad de tiempo. Se calcula como:

$$P = V \cdot I = I^2 \cdot R = \frac{V^2}{R}$$

Su unidad en el Sistema Internacional es el **Vatio (W)** o kilovatio ($1\text{ kW} = 1000\text{ W}$).

El **Efecto Joule** determina que toda corriente eléctrica que atraviesa una resistencia disipa calor según la energía térmica:

$$E = P \cdot t = I^2 \cdot R \cdot t$$

(medida en **Julios (J)** o en calorías, $1\text{ cal} \approx 0{,}24\text{ J}$).

---

## ¿Por qué importa?
1. **Piedra angular de la electrónica**: Permite predecir voltajes e intensidades en cualquier rama antes de realizar un montaje físico.
2. **Dimensionamiento de componentes**: Evita que los componentes se quemen al calcular la potencia que deben disipar (ej. resistencias de $1/4\text{ W}$, $1/2\text{ W}$ o $1\text{ W}$).
3. **Seguridad y eficiencia**: Esencial para dimensionar fusibles, secciones de cables e interruptores magnetotérmicos en instalaciones domésticas e industriales.

---

## ¿Cómo se aplica o relaciona?
* **En el taller**: Para limitar la corriente en diodos emisores de luz mediante [[diodos_y_leds]] y [[guia_calculo_proteccion_led]].
* **En análisis de circuitos**: Combinada con las reglas de [[asociacion_resistencias]] para resolver circuitos serie, paralelo y mixtos en [[guia_resolucion_circuitos_electricos]].
* **Fórmulas derivadas**:
  * $I = \frac{V}{R}$
  * $R = \frac{V}{I}$
  * $P = I^2 \cdot R$

### Ejemplo Práctico:
Una lámpara conectada a una batería de $12\text{ V}$ consume una corriente de $250\text{ mA}$ ($0{,}25\text{ A}$):
1. **Resistencia de la lámpara**: $R = \frac{V}{I} = \frac{12\text{ V}}{0{,}25\text{ A}} = 48\,\Omega$.
2. **Potencia consumida**: $P = V \cdot I = 12\text{ V} \cdot 0{,}25\text{ A} = 3\text{ W}$.
3. **Energía consumida en 1 hora ($3600\text{ s}$)**: $E = P \cdot t = 3\text{ W} \cdot 3600\text{ s} = 10800\text{ J} = 3\text{ W}\cdot\text{h}$.
