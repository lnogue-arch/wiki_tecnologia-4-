---
title: Banco de Exámenes Oficiales y Solucionarios de 4º ESO
tags: [examenes, solucionario, evaluacion, 4eso]
aliases: [Exámenes Tecnología 4º, Solucionario Exámenes]
---

# Banco de Exámenes Oficiales y Solucionarios de 4º ESO

Recopilación estructurada de los modelos de examen oficiales de todas las evaluaciones del curso.

---

## 1ª Evaluación: Electricidad y Electrónica Analógica

### Preguntas Teóricas Clave:
1. **Comportamiento del Diodo**:
   * Polarización directa (conduce a partir de $0{,}7\text{ V}$, resistencia interna prácticamente nula).
   * Polarización inversa (bloquea la corriente, actúa como circuito abierto).
2. **Transistor en Zona Activa**:
   * Unión Base-Emisor polarizada directamente ($V_{BE} \approx 0{,}7\text{ V}$), unión Base-Colector inversamente polarizada.
   * La corriente de colector es proporcional a la de base: $I_C = \beta \cdot I_B$.
3. **Cálculo de Código de Colores**:
   * Determinación de valores nominales y rangos máximos y mínimos con la tolerancia.

### Problemas Tipo Resueltos:
* **Circuito RC y Equivalentes**: Cálculo de $R_{eq}$ serie, $C_{eq}$ paralelo, constante $\tau = R_{eq} \cdot C_{eq}$ y tiempo de carga completa $t = 5\tau$.
* **Protección de LED**: $R = \frac{V_{cc} - V_{LED}}{I_{LED}}$.
* **Resistividad en Líneas**: $R = \rho \cdot \frac{L}{S}$.
* **Sensor con Termistor**: Cálculo de resistencia máxima/mínima según temperaturas y velocidad de giro del motor.

---

## 2ª Evaluación: Electrónica Digital y Puertas Lógicas

### Preguntas Teóricas Clave:
1. **Diferencia Señal Analógica vs Digital**: Continuidad de valores e inmunidad frente a ruido.
2. **Capacidad de Combinaciones Binarias**: Con $n$ bits se generan $2^n$ estados distintos.
3. **Postulados de Boole y De Morgan**: Demostración y simplificación de expresiones algebraicas.

### Problemas Tipo Resueltos:
* **Conversión Numérica**: Decimal a Binario, Binario a Hexadecimal, Unidades KB, MB, GB.
* **Problema Complejo de Diseño (Caso Túnel / Control Industrial)**:
  * Tabla de verdad (16 filas para 4 entradas $A, B, C, D$).
  * Extracción de minterms.
  * Simplificación por Mapa de Karnaugh de $4 \times 4$.
  * Dibujo del esquema circuital con puertas AND, OR, NOT.

---

## 3ª Evaluación: Robótica, Neumática y Arduino

### Preguntas Teóricas Clave:
1. **Definición y Clasificación de Robots**: Poliarticulados, móviles, androides, zoomórficos, híbridos.
2. **Sistemas de Control**: Lazo Abierto (sin sensor de realimentación) vs Lazo Cerrado (con feedback y control de error).
3. **Unidad de Mantenimiento Neumática (FRL)**: Funciones y componentes (Filtro, Regulador de presión con manómetro, Lubricador).
4. **Válvula de Simultaneidad**: Realiza la función lógica "Y" (AND) mediante accionamiento neumático puro.
5. **Arquitectura y Hardware Arduino**: Microcontrolador ATmega328P, pines digitales, pines PWM (~), entradas analógicas (ADC 10 bits).

### Problemas Tipo Resueltos:
* **Principio de Pascal (Problema del Hipopótamo de $1800\text{ kg}$)**: $\frac{F_1}{S_1} = \frac{F_2}{S_2} \Rightarrow F_1 = 145{,}8\text{ N}$.
* **Ecuación de Continuidad y Caudal ($90\text{ l/min}$)**: Conversión al SI y cálculo de velocidades $v_1$ y $v_2$ en estrechamientos.
* **Análisis de Código Arduino**: Explicación línea por línea de funciones `setup()`, `loop()`, `pinMode()`, `digitalWrite()`, `delay()`.

---
*Para consultar los documentos originales digitalizados, véase [[fuente_04_examenes_y_evaluaciones]].*
