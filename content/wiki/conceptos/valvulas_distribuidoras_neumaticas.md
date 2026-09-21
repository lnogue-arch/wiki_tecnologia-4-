---
title: Válvulas Distribuidoras Neumáticas y Cilindros
tags: [neumatica, valvulas, cilindros, actuadores, 3a_evaluacion, 4eso]
aliases: [Válvula Distribuidora, Cilindro Simple Efecto, Cilindro Doble Efecto, Válvula 3/2, Válvula 5/2]
---

# Válvulas Distribuidoras Neumáticas y Cilindros

## ¿Qué es?
Las **válvulas distribuidoras** son los elementos de mando que dirigen, regulan o bloquean el flujo de aire comprimido hacia los actuadores neumáticos.

### Nomenclatura y Designación ($N^\circ \text{Vías} / N^\circ \text{Posiciones}$):
* **Posiciones (cuadros)**: Número de estados estables que puede adoptar la válvula (cada posición se dibuja con un cuadrado contiguo). Típicamente $2$ o $3$ posiciones.
* **Vías (conexiones)**: Número de orificios o tomas de conexión externas que tiene la válvula (presión, escapes y salidas a actuadores).
  * **Vía 1 (P)**: Entrada de alimentación de presión de aire.
  * **Vías 2, 4 (A, B)**: Vías de trabajo o utilización que van hacia los cilindros.
  * **Vías 3, 5 (R, S)**: Vías de escape de aire a la atmósfera.

### Válvulas Distribuidoras Más Comunes:
1. **Válvula 2/2**: 2 vías y 2 posiciones (grifo de paso simple: abierto o cerrado).
2. **Válvula 3/2**: 3 vías y 2 posiciones. Ideal para controlar **cilindros de simple efecto**.
   * *NC (Normalmente Cerrada)*: En reposo la entrada 1 está bloqueada y la vía 2 comunica con el escape 3. Al accionarse, comunica 1 con 2.
   * *NA (Normalmente Abierta)*: En reposo comunica 1 con 2. Al accionarse, corta el aire.
3. **Válvula 5/2**: 5 vías y 2 posiciones. Esencial para gobernar **cilindros de doble efecto** (alterna la alimentación entre la cámara anterior y posterior del cilindro).

### Tipos de Accionamiento y Retorno:
* **Accionamientos**: Manual (pulsador, palanca, pedal), Mecánico (pulsador de leva, final de carrera por rodillo), Neumático (pilotaje por aire), Eléctrico (solenoide / electroválvula).
* **Retorno**: Generalmente por muelle (monoestable) o por doble pilotaje (biestable).

### Cilindros Neumáticos:
* **Cilindro de Simple Efecto**: Solo tiene una entrada de aire. El vástago avanza por presión de aire y retrocede por la acción de un muelle interno al cesar la presión.
* **Cilindro de Doble Efecto**: Posee dos tomas de aire. El vástago avanza con aire en la cámara trasera y retrocede con aire en la cámara delantera.

---

## ¿Por qué importa?
Permite materializar automatismos de transporte de piezas, prensado y clasificación industrial sin componentes electrónicos en ambientes con riesgo de explosión.

---

## ¿Cómo se aplica o relaciona?
* Se complementa con las funciones lógicas de [[valvulas_logicas_simultaneidad_selectora]].
* Representación esquemática normalizada en [[simbologia_neumatica_y_electronica]].
