---
title: Guía de Resolución de Problemas de Principio de Pascal y Continuidad
tags: [guia, neumatica, hidraulica, fisica, ejercicios, 3a_evaluacion, 4eso]
aliases: [Problemas Pascal, Problemas Continuidad, Prensa Hidráulica, Caudal]
---

# Guía de Resolución de Problemas de Principio de Pascal y Continuidad

## 1. Problemas de Prensa Hidráulica (Principio de Pascal)

### Ecuación Base:
$$\frac{F_1}{S_1} = \frac{F_2}{S_2} \quad \Longrightarrow \quad \frac{F_1}{d_1^2} = \frac{F_2}{d_2^2}$$

### Procedimiento Sistemático:
1. **Identificar datos y convertir unidades al Sistema Internacional**:
   * Fuerzas en Newtons ($N$). Si te dan masa en kilogramos: $F = m \cdot g$ ($g \approx 10\text{ m/s}^2$ o $9{,}8\text{ m/s}^2$).
   * Diámetros o radios en metros ($m$).
2. **Calcular superficies**:
   $$S = \pi \cdot r^2 = \pi \cdot \left(\frac{d}{2}\right)^2$$
3. **Despejar la incógnita**:
   * Fuerza necesaria: $F_1 = F_2 \cdot \frac{S_1}{S_2}$
   * Diámetro necesario: $d_1 = d_2 \cdot \sqrt{\frac{F_1}{F_2}}$

---

## 2. Problemas de Caudal y Ecuación de Continuidad

### Ecuaciones Base:
$$Q = S \cdot v = \text{constante}$$
$$S_1 \cdot v_1 = S_2 \cdot v_2$$

### Tabla de Factores de Conversión Obligatorios:

| Magnitud | Unidad Dada | Multiplicar por | Para Obtener en el SI |
| :--- | :--- | :--- | :--- |
| **Caudal ($Q$)** | $\text{litros/minuto}$ | $\frac{10^{-3}}{60} = \frac{1}{60000}$ | $\text{m}^3/\text{s}$ |
| **Caudal ($Q$)** | $\text{litros/segundo}$ | $10^{-3}$ | $\text{m}^3/\text{s}$ |
| **Sección ($S$)** | $\text{cm}^2$ | $10^{-4}$ ($0{,}0001$) | $\text{m}^2$ |
| **Sección ($S$)** | $\text{mm}^2$ | $10^{-6}$ ($0{,}000001$) | $\text{m}^2$ |

---

## 3. Ejercicios Completos Resueltos

### Problema 1 (Pascal - Elevador Hidráulico de Taller):
Se desea elevar un automóvil de $1500\text{ kg}$ situado sobre un pistón de $1{,}2\text{ m}$ de diámetro aplicando una fuerza sobre un pistón pequeño de $6\text{ cm}$ de diámetro. Calcula la fuerza necesaria $F_1$.
* $F_2 = 1500\text{ kg} \cdot 10\text{ m/s}^2 = 15000\text{ N}$.
* $d_2 = 1{,}2\text{ m} \Rightarrow r_2 = 0{,}6\text{ m} \Rightarrow S_2 = \pi \cdot 0{,}6^2 \approx 1{,}131\text{ m}^2$.
* $d_1 = 6\text{ cm} = 0{,}06\text{ m} \Rightarrow r_1 = 0{,}03\text{ m} \Rightarrow S_1 = \pi \cdot 0{,}03^2 \approx 0{,}002827\text{ m}^2$.
* **Cálculo de $F_1$**:
  $$F_1 = F_2 \cdot \frac{S_1}{S_2} = 15000 \cdot \frac{0{,}002827}{1{,}131} = 37{,}5\text{ N}$$
*(Equivalente a una masa de solo $3{,}75\text{ kg}$)*.

### Problema 2 (Continuidad en Tubería):
Por una tubería de $50\text{ mm}$ de diámetro circula aire a $4\text{ m/s}$. Si la tubería se estrecha a $25\text{ mm}$ de diámetro:
1. **Secciones**: $S_1 = \pi \cdot (0{,}025)^2 = 1{,}963 \cdot 10^{-3}\text{ m}^2$ ; $S_2 = \pi \cdot (0{,}0125)^2 = 0{,}4909 \cdot 10^{-3}\text{ m}^2$.
2. **Caudal**: $Q = S_1 \cdot v_1 = 1{,}963 \cdot 10^{-3} \cdot 4 = 7{,}85 \cdot 10^{-3}\text{ m}^3/\text{s}$.
3. **Velocidad en el estrechamiento**:
   $$v_2 = v_1 \cdot \frac{S_1}{S_2} = 4 \cdot \left(\frac{50}{25}\right)^2 = 4 \cdot 2^2 = 16\text{ m/s}$$
*(Al reducir el diámetro a la mitad, la velocidad se cuadruplica)*.

---
*Conceptos relacionados: [[neumatica_fuerza_presion_pascal]], [[caudal_y_ecuacion_continuidad]].*
