---
title: Válvulas Lógicas Neumáticas (Simultaneidad, Selectora y Regulación)
tags: [neumatica, valvulas_logicas, funcion_and, funcion_or, 3a_evaluacion, 4eso]
aliases: [Válvula de Simultaneidad, Válvula Selectora, Función AND Neumática, Función OR Neumática]
---

# Válvulas Lógicas Neumáticas (Simultaneidad, Selectora y Regulación)

## ¿Qué es?
En neumática pura existen componentes mecánicos capaces de realizar operaciones lógicas binarias sin necesidad de recurrir a la electricidad ni a la electrónica:

### 1. Válvula de Simultaneidad (Función Lógica "Y" / AND)
* **Comportamiento**: Tiene dos entradas de señal ($1$ y $1$) y una salida ($2$). Para que el aire salga por la vía $2$, **es obligatorio que exista presión simultáneamente en AMBAS entradas $1$**.
* **Mecanismo interno**: Un pistón móvil obtura la salida si solo entra aire por un lado. Solo cuando entra aire por ambos extremos con igual presión se permite el paso hacia la salida.
* **Aplicación de seguridad**: Mando bimano de seguridad en prensas industriales y guillotinas (obliga al operario a accionar dos pulsadores a la vez con ambas manos para evitar amputaciones).

### 2. Válvula Selectora o de Doble Efecto (Función Lógica "O" / OR)
* **Comportamiento**: Tiene dos entradas ($1$ y $1$) y una salida ($2$). El aire sale por la vía $2$ si entra presión por **CUALQUIERA de las dos entradas** (o por ambas).
* **Mecanismo interno**: Una bola obturadora bascula taponando la entrada que carece de presión e impidiendo que el aire se escape por ella, dirigiéndolo hacia la salida 2.
* **Aplicación**: Mando de un cilindro desde dos puestos de control diferentes (ej. pulsador manual local o pedal remoto).

### 3. Válvula Reguladora de Caudal Unidireccional
* Formada por un estrangulamiento regulable en paralelo con una válvula antirretorno.
* Permite regular la velocidad de salida del vástago de un cilindro en un sentido, mientras que el retroceso se produce a máxima velocidad sin retención.

---

## ¿Por qué importa?
Permite diseñar autómatas neumáticos puros extremadamente robustos, resistentes a humedad, polvo, altas temperaturas e interferencias electromagnéticas.

---

## ¿Cómo se aplica o relaciona?
* Comparar con las puertas lógicas electrónicas en [[puertas_logicas_fundamentales]].
* Esquemas normalizados ISO 1219 en [[simbologia_neumatica_y_electronica]].
