---
title: Sistemas de Numeración (Decimal, Binario y Hexadecimal)
tags: [matematicas_digitales, binario, hexadecimal, 2a_evaluacion, 4eso]
aliases: [Binario, Hexadecimal, Conversión de Bases, Bit y Byte]
---

# Sistemas de Numeración (Decimal, Binario y Hexadecimal)

## ¿Qué es?
Los sistemas de numeración posicionales representan cantidades numéricas mediante una base $b$ y un conjunto de símbolos o dígitos:

### 1. Sistema Decimal (Base 10)
* Dígitos: $0, 1, 2, 3, 4, 5, 6, 7, 8, 9$.
* Valor posicional: Cada posición multiplica por potencias de $10$ ($10^0, 10^1, 10^2, \dots$).

### 2. Sistema Binario (Base 2)
* Dígitos: $0, 1$ (denominados **bits** = *binary digits*).
* Valor posicional: Cada posición multiplica por potencias de $2$ ($1, 2, 4, 8, 16, 32, 64, 128, \dots$).
* Con $n$ bits se pueden codificar **$2^n$ combinaciones o estados diferentes** (desde $0$ hasta $2^n - 1$).
  * Para $n=3$ bits: $2^3 = 8$ combinaciones ($000_2$ a $111_2$, es decir, de $0$ a $7$).
  * Para $n=4$ bits: $2^4 = 16$ combinaciones ($0000_2$ a $1111_2$, de $0$ a $15$).
  * Para $n=8$ bits (1 Byte): $2^8 = 256$ combinaciones (de $0$ a $255$).

### 3. Sistema Hexadecimal (Base 16)
* Dígitos: $0, 1, 2, 3, 4, 5, 6, 7, 8, 9, \text{A}(=10), \text{B}(=11), \text{C}(=12), \text{D}(=13), \text{E}(=14), \text{F}(=15)$.
* Cada dígito hexadecimal equivale exactamente a **un grupo de 4 bits binarios (nibble)**.

### Unidades de Información Digital:
* **Bit**: Unidad mínima de información ($0$ o $1$).
* **Byte (B)**: Conjunto de $8$ bits.
* **Kilobyte (KB)**: $1024\text{ Bytes} = 2^{10}\text{ B}$ (o $1000\text{ B}$ según SI).
* **Megabyte (MB)**: $1024\text{ KB} = 2^{20}\text{ B}$.
* **Gigabyte (GB)**: $1024\text{ MB} = 2^{30}\text{ B}$.

---

## ¿Por qué importa?
1. **Idioma nativo del hardware**: Los circuitos digitales solo entienden la presencia ('1') o ausencia ('0') de voltaje en sus transistores.
2. **Direccionamiento de memoria y colores**: El código hexadecimal se utiliza en informática para compactar cadenas binarias largas (ej. colores web `#FF0000`, direcciones MAC).

---

## ¿Cómo se aplica o relaciona?
* Fundamento de las tablas de verdad en [[puertas_logicas_fundamentales]] y [[mapas_de_karnaugh]].
* Comunicación serie y manejo de registros en [[registro_desplazamiento_74hc595]].

### Métodos de Conversión:
* **Binario $\rightarrow$ Decimal**: Multiplicar cada bit por su potencia de 2:
  $$1101_2 = 1 \cdot 2^3 + 1 \cdot 2^2 + 0 \cdot 2^1 + 1 \cdot 2^0 = 8 + 4 + 0 + 1 = 13_{10}$$
* **Decimal $\rightarrow$ Binario**: Divisiones sucesivas entre 2 recogiendo los restos en orden inverso.
* **Binario $\rightarrow$ Hexadecimal**: Agrupar en bloques de 4 bits de derecha a izquierda:
  $$1101\;1010_2 = \text{D}\;\text{A}_{16} = 0\text{xDA}$$
