---
title: Guía de Cálculo y Selección de la Resistencia de Protección para LEDs
tags: [guia, led, calculo, 1a_evaluacion, 4eso]
aliases: [Resistencia de LED, Cálculo LED]
---

# Guía de Cálculo y Selección de la Resistencia de Protección para LEDs

## 1. El Problema Técnico
Un diodo LED nunca debe conectarse directamente a una fuente de alimentación de voltaje fijo (como una pila de 9V, una fuente de 12V o los 5V de Arduino) porque su resistencia interna en conducción es casi nula. Sin una resistencia limitadora, la corriente aumentaría por encima del máximo admisible (típicamente $20-30\text{ mA}$), destruyendo el componente por sobrecalentamiento instantáneo.

---

## 2. Ecuación de Diseño

$$R = \frac{V_{cc} - V_{LED}}{I_{LED}}$$

Donde:
* **$V_{cc}$**: Tensión de la fuente de alimentación (V).
* **$V_{LED}$**: Caída de tensión directa del LED (según su color):
  * **Rojo / Naranja**: $1{,}8\text{ V} - 2{,}0\text{ V}$
  * **Amarillo**: $2{,}0\text{ V} - 2{,}1\text{ V}$
  * **Verde**: $2{,}2\text{ V}$
  * **Azul / Blanco / UV**: $3{,}0\text{ V} - 3{,}3\text{ V}$
* **$I_{LED}$**: Intensidad de diseño deseada en Amperios (normalmente $10\text{ mA} = 0{,}01\text{ A}$ para señalización tenue o $20\text{ mA} = 0{,}02\text{ A}$ para brillo pleno).

---

## 3. Selección del Valor Comercial (Serie E12)
El valor calculado casi nunca coincide con un valor comercial exacto. Se debe escoger el **valor comercial inmediatamente superior** de la serie normalizada E12:
$$10, 12, 15, 18, 22, 27, 33, 39, 47, 56, 68, 82 \quad (\times 10^n)$$

---

## 4. Cálculo de la Potencia Disipada
Para asegurar que la resistencia no se queme:
$$P_R = I_{LED}^2 \cdot R = (V_{cc} - V_{LED}) \cdot I_{LED}$$
Si $P_R < 0{,}25\text{ W}$, se utiliza una resistencia estándar de $1/4\text{ W}$.

---

## 5. Ejemplos Prácticos

### Caso A: LED Rojo conectado a Arduino ($5\text{ V}$)
* $V_{cc} = 5\text{ V}$
* $V_{LED} = 2\text{ V}$
* $I_{LED} = 15\text{ mA} = 0{,}015\text{ A}$
* **Cálculo**:
  $$R = \frac{5 - 2}{0{,}015} = \frac{3}{0{,}015} = 200\,\Omega$$
* **Selección comercial E12**: **$220\,\Omega$** (Rojo - Rojo - Marrón - Oro).

### Caso B: LED Verde conectado a Batería de Coche ($12\text{ V}$)
* $V_{cc} = 12\text{ V}$
* $V_{LED} = 2\text{ V}$
* $I_{LED} = 20\text{ mA} = 0{,}02\text{ A}$
* **Cálculo**:
  $$R = \frac{12 - 2}{0{,}02} = \frac{10}{0{,}02} = 500\,\Omega$$
* **Selección comercial E12**: **$560\,\Omega$** (Verde - Azul - Marrón - Oro) o $470\,\Omega$.

---
*Conceptos relacionados: [[diodos_y_leds]], [[codigo_colores_resistencias]], [[ley_de_ohm_y_potencia]].*
