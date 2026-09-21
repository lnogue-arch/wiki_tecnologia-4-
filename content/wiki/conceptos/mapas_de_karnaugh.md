---
title: Mapas de Karnaugh (Simplificación Gráfica)
tags: [karnaugh, simplificacion, electronica_digital, 2a_evaluacion, 4eso]
aliases: [Mapa de Karnaugh, Karnaugh Maps, Simplificación Booleana]
---

# Mapas de Karnaugh (Simplificación Gráfica)

## ¿Qué es?
Un **mapa de Karnaugh** es un método gráfico matricial utilizado para simplificar funciones booleanas de manera directa y visual, minimizando el riesgo de errores algebraicos.

### Estructura de las Celdas:
* Para $N$ variables de entrada, el mapa tiene **$2^N$ celdas**.
  * 2 Variables ($A, B$): Matriz $2 \times 2$ (4 celdas).
  * 3 Variables ($A, B, C$): Matriz $2 \times 4$ (8 celdas).
  * 4 Variables ($A, B, C, D$): Matriz $4 \times 4$ (16 celdas).
* **Ordenamiento en Código Gray**: Las filas y columnas contiguas cambian únicamente en **1 bit a la vez**:
  $$\text{Secuencia: } 00 \rightarrow 01 \rightarrow 11 \rightarrow 10$$
  *(¡Atención! El orden NO es $00, 01, 10, 11$, sino que se permutan los dos últimos para garantizar la adyacencia lógica)*.

### Reglas de Agrupación de 1s (Minterms):
1. **Tamaño de los grupos**: Los grupos deben contener una cantidad de celdas que sea **potencia de 2**: $1, 2, 4, 8$ o $16$. *(Nunca grupos de 3, 5 o 6)*.
2. **Forma rectangular**: Los grupos deben ser rectángulos o cuadrados contiguos.
3. **Máximo tamaño**: Los grupos deben ser lo más grandes posible (un grupo más grande elimina más variables).
4. **Mínimo número de grupos**: Todo '1' debe estar incluido al menos en un grupo, pero evitando grupos redundantes.
5. **Solapamiento y Adyacencia Tórica**: Los grupos pueden solaparse y las celdas de los extremos opuestos (bordes izquierdo-derecho y superior-inferior, incluidas las 4 esquinas) son adyacentes.

### Extracción del Término Simplificado:
Por cada grupo formado:
* Se observan las variables correspondientes a sus celdas.
* Si una variable **cambia de estado** ($0$ y $1$ dentro del grupo), **se elimina**.
* Si una variable **mantiene su estado**, **se conserva** (en forma directa $A$ si vale $1$, o negada $\overline{A}$ si vale $0$).

---

## ¿Por qué importa?
Es la herramienta reina en 4º de ESO para resolver problemas de ingeniería donde un enunciado verbal se traduce en un circuito electrónico eficiente.

---

## ¿Cómo se aplica o relaciona?
* Sigue la guía paso a paso con el caso del túnel contra incendios en [[guia_diseno_digital_karnaugh_paso_a_paso]].
* Complemento teórico de [[algebra_de_boole_y_de_morgan]] y [[puertas_logicas_fundamentales]].
