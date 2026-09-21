---
title: Álgebra de Boole y Teoremas de De Morgan
tags: [algebra_de_boole, logica_digital, matematicas, 2a_evaluacion, 4eso]
aliases: [Álgebra de Boole, Teoremas de De Morgan, Simplificación Lógica]
---

# Álgebra de Boole y Teoremas de De Morgan

## ¿Qué es?
El **Álgebra de Boole** es una estructura matemática desarrollada por George Boole para formalizar la lógica proposicional. En electrónica digital, las variables solo adoptan valores $0$ o $1$, y se definen tres operaciones básicas:
1. **Suma lógica (OR)**: $A + B$ (Disyunción)
2. **Producto lógico (AND)**: $A \cdot B$ (Conjunción)
3. **Negación lógica (NOT)**: $\overline{A}$ o $A'$ (Complemento)

### Postulados y Propiedades Fundamentales:

| Propiedad | Suma (OR) | Producto (AND) |
| :--- | :--- | :--- |
| **Identidad** | $A + 0 = A$ | $A \cdot 1 = A$ |
| **Elemento nulo (absorción)** | $A + 1 = 1$ | $A \cdot 0 = 0$ |
| **Idempotencia** | $A + A = A$ | $A \cdot A = A$ |
| **Complementación** | $A + \overline{A} = 1$ | $A \cdot \overline{A} = 0$ |
| **Involución (Doble negación)** | $\overline{\overline{A}} = A$ | - |
| **Conmutativa** | $A + B = B + A$ | $A \cdot B = B \cdot A$ |
| **Asociativa** | $(A + B) + C = A + (B + C)$ | $(A \cdot B) \cdot C = A \cdot (B \cdot C)$ |
| **Distributiva** | $A + (B \cdot C) = (A + B) \cdot (A + C)$ | $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$ |
| **Absorción general** | $A + A \cdot B = A$ | $A \cdot (A + B) = A$ |
| **Absorción secundaria** | $A + \overline{A} \cdot B = A + B$ | $A \cdot (\overline{A} + B) = A \cdot B$ |

### Teoremas de De Morgan:
Permiten transformar sumas lógicas en productos y viceversa mediante negación global:

$$\text{1er Teorema: } \overline{A + B} = \overline{A} \cdot \overline{B}$$
$$\text{2º Teorema: } \overline{A \cdot B} = \overline{A} + \overline{B}$$

*Regla mnemotécnica*: "Rompe la barra y cambia el signo".

---

## ¿Por qué importa?
1. **Optimización de circuitos**: Permite reducir el número de puertas lógicas y circuitos integrados necesarios, abaratando costes y reduciendo el consumo energético.
2. **Conversión a puertas universales**: Facilita implementar cualquier función usando exclusivamente puertas NAND o NOR.

---

## ¿Cómo se aplica o relaciona?
* Es la base formal para la simplificación que se agiliza gráficamente en [[mapas_de_karnaugh]].
* Se implementa físicamente mediante [[puertas_logicas_fundamentales]].
* Metodología de diseño completa en [[guia_diseno_digital_karnaugh_paso_a_paso]].
