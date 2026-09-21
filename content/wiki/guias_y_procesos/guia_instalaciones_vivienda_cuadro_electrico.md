---
title: Guía de Dimensionamiento y Análisis del Cuadro Eléctrico de una Vivienda
tags: [guia, instalaciones, vivienda, cgmp, calculo_potencia, 4eso]
aliases: [Guía Cuadro Eléctrico, Cálculo de PIAs, Análisis CGMP]
---

# Guía de Dimensionamiento y Análisis del Cuadro Eléctrico de una Vivienda

## 1. Clasificación de Grados de Electrificación (REBT)

En España, las viviendas se clasifican según su previsión de potencia eléctrica en dos grados:
* **Grado de Electrificación Básico ($5750\text{ W}$ a $230\text{ V} \Rightarrow 25\text{ A}$)**:
  * Cubre las necesidades primarias de alumbrado, pequeños electrodomésticos, cocina eléctrica, horno, lavadora y termo.
  * Obligatorio contar al menos con los circuitos **C1, C2, C3, C4 y C5**.
* **Grado de Electrificación Elevado ($9200\text{ W} \Rightarrow 40\text{ A}$)**:
  * Obligatorio si la vivienda tiene una superficie útil $>160\text{ m}^2$, o dispone de aire acondicionado canalizado, calefacción eléctrica, secadora independiente o domótica avanzada.
  * Incorpora circuitos adicionales: **C6** (adicional de iluminación), **C7** (adicional de tomas), **C8** (calefacción), **C9** (aire acondicionado), **C10** (secadora), **C11** (domótica).

---

## 2. Metodología de Cálculo y Dimensionamiento

### Paso 1: Cálculo de la Intensidad Nominal por Receptor
Aplicando la [[ley_de_ohm_y_potencia]] en corriente alterna monofásica ($230\text{ V}$):

$$I = \frac{P}{V}$$

* *Ejemplo (Horno eléctrico de $2300\text{ W}$)*:
  $$I = \frac{2300\text{ W}}{230\text{ V}} = 10\text{ A}$$
* *Ejemplo (Vitrocerámica a máxima potencia de $5750\text{ W}$)*:
  $$I = \frac{5750\text{ W}}{230\text{ V}} = 25\text{ A}$$

### Paso 2: Elección del Magnetotérmico (PIA) y Sección de Cable
La corriente nominal del PIA ($I_n$) debe ser superior a la corriente máxima del circuito, pero inferior a la máxima corriente que puede soportar el cable sin sobrecalentarse:

$$I_{\text{circuito}} \le I_{n,\text{PIA}} \le I_{\text{admisible cable}}$$

---

## 3. Protocolo de Comprobación y Seguridad
1. **Comprobación del Diferencial**: Pulsar mensualmente el botón de test **T**. El mecanismo debe dispararse de forma instantánea. Si no salta, el diferencial está averiado y debe sustituirse de inmediato.
2. **Resistencia de Puesta a Tierra**: Verificar con telurómetro que la resistencia del electrodo de tierra es inferior a $15-30\,\Omega$.

---
*Conceptos relacionados: [[instalaciones_vivienda_electricidad_cgmp]], [[ley_de_ohm_y_potencia]], [[esquemas_instalaciones_y_cgmp]].*
