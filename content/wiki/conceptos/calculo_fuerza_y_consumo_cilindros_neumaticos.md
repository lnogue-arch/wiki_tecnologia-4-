---
title: Cálculo de Fuerza y Consumo en Cilindros Neumáticos e Hidráulicos
tags: [neumatica, hidraulica, cilindros, calculo_fuerzas, 3a_evaluacion, 4eso]
aliases: [Fuerza de Cilindro, Fuerza de Avance y Retroceso, Consumo Neumático]
---

# Cálculo de Fuerza y Consumo en Cilindros Neumáticos e Hidráulicos

## 1. Tipos de Presión y Unidades
* **Presión Atmosférica ($P_{atm}$)**: Presión ejercida por la columna de aire de la atmósfera a nivel del mar ($P_{atm} pprox 1	ext{ bar} = 10^5	ext{ Pa} = 100	ext{ kPa}$).
* **Presión Relativa o Manométrica ($P_{rel}$)**: Presión medida por el manómetro del compresor respecto a la presión atmosférica (es la presión de trabajo $P$).
* **Presión Absoluta ($P_{abs}$)**:
  $$P_{abs} = P_{atm} + P_{rel}$$

---

## 2. Fuerzas Teóricas en un Cilindro de Doble Efecto

Un cilindro de doble efecto tiene dos secciones útiles diferentes debido a la presencia del vástago metálico en la cámara delantera:

```text
                     CÁMARA TRASERA (Avance)        CÁMARA DELANTERA (Retroceso)
                     +---------------------------+--+------------------------+
                     |                           |  |                        |
        AIRE AVANCE  |======>                    |  |===[ VÁSTAGO ]========> | AIRE RETROCESO
         (Vía 1)     |                           |  |  (Sección Sv)          |  (Vía 2)
                     +---------------------------+--+------------------------+
                     |<------ Sección Sp ------->|  |<-- Sección (Sp - Sv) ->|
```

### A. Fuerza Teórica de Avance ($F_{av}$)
Toda la superficie del émbolo ($S_p$) recibe la presión del aire:
$$S_p = \pi \cdot R^2 = rac{\pi \cdot D^2}{4}$$
$$F_{av} = P \cdot S_p$$

### B. Fuerza Teórica de Retroceso ($F_{ret}$)
La superficie efectiva ($S_{útil}$) es la sección del émbolo menos la sección del vástago ($S_v$):
$$S_v = rac{\pi \cdot d^2}{4}$$
$$S_{útil} = S_p - S_v = rac{\pi \cdot (D^2 - d^2)}{4}$$
$$F_{ret} = P \cdot S_{útil} = P \cdot (S_p - S_v)$$

* **Consecuencia física**: Para una misma presión de trabajo $P$, la **fuerza de avance siempre es mayor que la fuerza de retroceso** ($F_{av} > F_{ret}$).

---

## 3. Ejemplo Práctico Resuelto de Examen:
Un cilindro neumático de doble efecto tiene un émbolo de diámetro $D = 80	ext{ mm}$ ($0{,}08	ext{ m}$) y un vástago de $d = 20	ext{ mm}$ ($0{,}02	ext{ m}$), trabajando a una presión de $P = 6	ext{ bar} = 6 \cdot 10^5	ext{ Pa}$.
1. **Sección del émbolo**:
   $$S_p = rac{\pi \cdot (0{,}08)^2}{4} pprox 5{,}026 \cdot 10^{-3}	ext{ m}^2$$
2. **Sección del vástago**:
   $$S_v = rac{\pi \cdot (0{,}02)^2}{4} pprox 3{,}141 \cdot 10^{-4}	ext{ m}^2$$
3. **Fuerza de avance**:
   $$F_{av} = 6 \cdot 10^5	ext{ Pa} \cdot 5{,}026 \cdot 10^{-3}	ext{ m}^2 = 3015{,}6	ext{ N} pprox 301{,}5	ext{ kg}$$
4. **Fuerza de retroceso**:
   $$S_{útil} = (5{,}026 - 0{,}314) \cdot 10^{-3} = 4{,}712 \cdot 10^{-3}	ext{ m}^2$$
   $$F_{ret} = 6 \cdot 10^5	ext{ Pa} \cdot 4{,}712 \cdot 10^{-3}	ext{ m}^2 = 2827{,}2	ext{ N} pprox 282{,}7	ext{ kg}$$

---
*Conceptos relacionados: [[neumatica_fuerza_presion_pascal]], [[valvulas_distribuidoras_neumaticas]], [[circuito_neumatico_frl_compresor]].*
