---
title: Resistividad y Resistencia de Conductores
tags: [electricidad, materiales, conductores, 1a_evaluacion, 4eso]
aliases: [Resistividad, Resistencia de un cable]
---

# Resistividad y Resistencia de Conductores

## ¿Qué es?
La resistencia eléctrica que ofrece un conductor metálico homogéneo depende de sus dimensiones geométricas y de una propiedad intrínseca del material denominada **resistividad** ($\rho$):

$$R = \rho \cdot \frac{L}{S}$$

Donde:
* **$R$**: Resistencia eléctrica del conductor ($\Omega$).
* **$\rho$** (rho): **Resistividad** del material ($\Omega \cdot \text{m}$ o en unidades técnicas $\frac{\Omega \cdot \text{mm}^2}{\text{m}}$). Es inversamente proporcional a la conductividad ($\sigma = 1/\rho$).
* **$L$**: Longitud del conductor (metros, $\text{m}$).
* **$S$**: Sección transversal o área del cable (metros cuadrados $\text{m}^2$ o milímetros cuadrados $\text{mm}^2$). Para un cable circular de radio $r$ o diámetro $d$:

$$S = \pi \cdot r^2 = \pi \cdot \left(\frac{d}{2}\right)^2 = \frac{\pi \cdot d^2}{4}$$

### Resistividades típicas a $20^\circ\text{C}$:
* **Plata**: $1{,}59 \times 10^{-8}\,\Omega\cdot\text{m}$ (mejor conductor)
* **Cobre**: $1{,}72 \times 10^{-8}\,\Omega\cdot\text{m}$ (estándar en cableado eléctrico)
* **Aluminio**: $2{,}82 \times 10^{-8}\,\Omega\cdot\text{m}$ (líneas de alta tensión por ligereza)
* **Constantán / Nicrom**: $49 \times 10^{-8} - 100 \times 10^{-8}\,\Omega\cdot\text{m}$ (resistencias calefactoras)

---

## ¿Por qué importa?
1. **Caída de tensión en líneas largas**: En el transporte de energía eléctrica a larga distancia, la resistencia del cable provoca pérdidas por efecto Joule y caídas de voltaje.
2. **Selección del calibre del cable**: En instalaciones eléctricas de viviendas e industrias, dimensionar una sección insuficiente provoca sobrecalentamiento y riesgo de incendio.
3. **Diseño de elementos calefactores**: Permite calibrar la longitud y grosor del hilo de nicrom para radiadores, tostadoras o soldadores de estaño.

---

## ¿Cómo se aplica o relaciona?
* Se relaciona directamente con la [[ley_de_ohm_y_potencia]].
* Base para los ejercicios clásicos de exámenes de 4º ESO en [[banco_examenes_y_solucionarios]].

### Ejemplo de Examen:
Calcula la resistencia de un cable de cobre de $2\text{ mm}$ de diámetro y $10\text{ km}$ de longitud ($\\rho_{\text{Cu}} = 1{,}7 \cdot 10^{-8}\,\Omega\cdot\text{m}$):
1. **Radio del cable**: $r = 1\text{ mm} = 10^{-3}\text{ m}$.
2. **Sección transversal**: $S = \pi \cdot r^2 = \pi \cdot (10^{-3})^2 \approx 3{,}1416 \cdot 10^{-6}\text{ m}^2$.
3. **Longitud**: $L = 10\text{ km} = 10000\text{ m} = 10^4\text{ m}$.
4. **Resistencia**:
$$R = 1{,}7 \cdot 10^{-8} \cdot \frac{10^4}{3{,}1416 \cdot 10^{-6}} = \frac{1{,}7 \cdot 10^{-4}}{3{,}1416 \cdot 10^{-6}} \approx 54{,}11\,\Omega$$
