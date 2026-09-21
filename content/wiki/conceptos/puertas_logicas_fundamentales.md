---
title: Puertas Lógicas Fundamentales
tags: [puertas_logicas, electronica_digital, circuitos_combinacionales, 2a_evaluacion, 4eso]
aliases: [Puertas Lógicas, NOT, AND, OR, NAND, NOR, XOR, XNOR]
---

# Puertas Lógicas Fundamentales

## ¿Qué es?
Las **puertas lógicas** son bloques constructivos electrónicos que realizan las operaciones elementales del [[algebra_de_boole_y_de_morgan]]. Tienen una o más entradas digitales y una única salida digital.

### Catálogo de Puertas Lógicas:

#### 1. Puerta NOT (Inversor / Negador)
* **Función**: $S = \overline{A}$
* **Comportamiento**: La salida es el valor inverso de la entrada.
* *CI estándar*: 7404 (Hex Inverter).

#### 2. Puerta AND (Y / Multiplicación Lógica)
* **Función**: $S = A \cdot B$
* **Comportamiento**: La salida es $1$ **únicamente cuando todas** las entradas valen $1$.
* *CI estándar*: 7408 (Quad 2-input AND).

#### 3. Puerta OR (O / Suma Lógica)
* **Función**: $S = A + B$
* **Comportamiento**: La salida es $1$ si **al menos una** de las entradas vale $1$.
* *CI estándar*: 7432 (Quad 2-input OR).

#### 4. Puerta NAND (NO-Y / Producto Negado)
* **Función**: $S = \overline{A \cdot B}$
* **Comportamiento**: La salida es $0$ únicamente si todas las entradas valen $1$. Es una **puerta universal** (permite construir cualquier otra puerta).
* *CI estándar*: 7400.

#### 5. Puerta NOR (NO-O / Suma Negada)
* **Función**: $S = \overline{A + B}$
* **Comportamiento**: La salida es $1$ únicamente si todas las entradas valen $0$. También es una **puerta universal**.
* *CI estándar*: 7402.

#### 6. Puerta XOR (O Exclusiva)
* **Función**: $S = A \oplus B = \overline{A}B + A\overline{B}$
* **Comportamiento**: La salida es $1$ si las entradas son **distintas entre sí** ($01$ o $10$).
* *CI estándar*: 7486.

#### 7. Puerta XNOR (Equivalencia / NO-O Exclusiva)
* **Función**: $S = \overline{A \oplus B} = A B + \overline{A}\,\overline{B}$
* **Comportamiento**: La salida es $1$ si las entradas son **iguales entre sí** ($00$ o $11$).

---

## ¿Por qué importa?
1. **Bloques constructivos digitales**: Toda CPU, GPU o microcontrolador está compuesto por millones de estas puertas interconectadas.
2. **Implementación de algoritmos por hardware**: Permiten ejecutar decisiones lógicas en nanosegundos sin esperas de software.

---

## ¿Cómo se aplica o relaciona?
* Consulta la tabla visual completa en [[tablas_verdad_puertas]].
* Para simplificar combinaciones de puertas usa [[mapas_de_karnaugh]] y [[guia_diseno_digital_karnaugh_paso_a_paso]].
* Simulación en software: [[guia_simulacion_crocodile_technology]].
