---
title: Referencia Completa de Tablas de Verdad de Puertas Lógicas
tags: [assets, tablas_de_verdad, puertas_logicas, 2a_evaluacion, 4eso]
---

# Referencia Completa de Tablas de Verdad de Puertas Lógicas

### Puertas de 1 Entrada (NOT)

| Entrada $A$ | Salida $\overline{A}$ |
| :---: | :---: |
| 0 | **1** |
| 1 | **0** |

---

### Puertas de 2 Entradas (AND, OR, NAND, NOR, XOR, XNOR)

| $A$ | $B$ | AND ($A \cdot B$) | OR ($A + B$) | NAND ($\overline{A \cdot B}$) | NOR ($\overline{A + B}$) | XOR ($A \oplus B$) | XNOR ($\overline{A \oplus B}$) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | **0** | **0** | **1** | **1** | **0** | **1** |
| 0 | 1 | **0** | **1** | **1** | **0** | **1** | **0** |
| 1 | 0 | **0** | **1** | **1** | **0** | **1** | **0** |
| 1 | 1 | **1** | **1** | **0** | **0** | **0** | **1** |

---

### Resumen de Expresiones Booleanas:
* **NOT**: $S = \overline{A}$
* **AND**: $S = A \cdot B$
* **OR**: $S = A + B$
* **NAND**: $S = \overline{A \cdot B} = \overline{A} + \overline{B}$ (Teorema de De Morgan)
* **NOR**: $S = \overline{A + B} = \overline{A} \cdot \overline{B}$ (Teorema de De Morgan)
* **XOR**: $S = A \oplus B = A\overline{B} + \overline{A}B$
* **XNOR**: $S = \overline{A \oplus B} = AB + \overline{A}\,\overline{B}$

---
*Conceptos relacionados: [[puertas_logicas_fundamentales]], [[algebra_de_boole_y_de_morgan]], [[mapas_de_karnaugh]].*
