---
title: Diodos Semiconductores y Diodos LED
tags: [semiconductores, diodos, led, 1a_evaluacion, 4eso]
aliases: [Diodo, LED, Polarización Directa e Inversa, Diodo Zener]
---

# Diodos Semiconductores y Diodos LED

## ¿Qué es?
Un **diodo** es un componente semiconductor de dos terminales (Ánodo y Cátodo) formado por una unión P-N que actúa como una **válvula antirretorno eléctrica**: permite el paso de corriente en un único sentido y lo bloquea en el contrario.

### Modos de Polarización:
1. **Polarización Directa** ($V_{\text{Ánodo}} > V_{\text{Cátodo}}$):
   * Superada la tensión de umbral ($V_d \approx 0{,}7\text{ V}$ para silicio, $0{,}3\text{ V}$ para germanio), el diodo **conduce** ofreciendo una resistencia prácticamente nula (actúa como interruptor cerrado).
2. **Polarización Inversa** ($V_{\text{Ánodo}} < V_{\text{Cátodo}}$):
   * La unión bloquea la corriente (salvo una minúscula corriente de fuga en picoamperios). Actúa como **interruptor abierto**.

### Diodo Emisor de Luz (LED - Light Emitting Diode):
* Diodo semiconductor especial (de Arseniuro de Galio, Nitruro de Galio, etc.) que emite fotones visibles cuando se polariza directamente por recombinación de pares electrón-hueco.
* **Caídas de tensión típicas ($V_{LED}$)**:
  * Rojo / Amarillo: $\approx 1{,}8\text{ V} - 2{,}0\text{ V}$
  * Verde: $\approx 2{,}2\text{ V}$
  * Azul / Blanco: $\approx 3{,}0\text{ V} - 3{,}4\text{ V}$
* **Corriente nominal de funcionamiento**: $I_{LED} \approx 10\text{ mA} - 20\text{ mA}$ ($0{,}01\text{ A} - 0{,}02\text{ A}$).

### Identificación Física de Polaridad en un LED:
* **Ánodo (+)**: Patilla más larga; electrodo interno más pequeño.
* **Cátodo (-)**: Patilla más corta; parte achatada (chaflán) en el borde de la cápsula de plástico; electrodo interno tipo "bandera" más ancho.

---

## ¿Por qué importa?
1. **Rectificación**: Permite convertir la corriente alterna de la red en corriente continua mediante puentes rectificadores de diodos.
2. **Protección contra polaridad inversa**: Impide que conectar una batería al revés destruya circuitos electrónicos sensibles.
3. **Eficiencia en iluminación y señalización**: Los LEDs ofrecen una eficiencia energética $>85\%$ superior a las bombillas incandescentes.

---

## ¿Cómo se aplica o relaciona?
* **Cálculo de la Resistencia de Protección**: Guía paso a paso en [[guia_calculo_proteccion_led]].
* Aplicación de diodo volante en [[rele_electromecanico]].
* Prácticas de semáforos en [[guia_programacion_arduino_semaforos]].

### Fórmula de Protección del LED:
$$R_{\text{prot}} = \frac{V_{cc} - V_{LED}}{I_{LED}}$$
