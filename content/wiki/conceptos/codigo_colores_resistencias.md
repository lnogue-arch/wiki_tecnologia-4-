---
title: Código de Colores de Resistencias
tags: [componentes, electronica_analogica, medicion, 1a_evaluacion, 4eso]
aliases: [Código de Colores, Resistencias Fijas]
---

# Código de Colores de Resistencias

## ¿Qué es?
El **código de colores** es un sistema internacional estandarizado (norma IEC 60062) que permite identificar el valor nominal de la resistencia eléctrica (en Ohmios, $\Omega$) y su tolerancia porcentual mediante bandas de color impresas sobre el cuerpo cerámico del componente.

### Tabla de Bandas (Código de 4 Bandas):

| Color | 1ª Banda (1er Dígito) | 2ª Banda (2º Dígito) | 3ª Banda (Multiplicador) | 4ª Banda (Tolerancia) |
| :--- | :---: | :---: | :---: | :---: |
| **Negro** | 0 | 0 | $\times 10^0$ ($1$) | - |
| **Marrón** | 1 | 1 | $\times 10^1$ ($10$) | $\pm 1\%$ |
| **Rojo** | 2 | 2 | $\times 10^2$ ($100$) | $\pm 2\%$ |
| **Naranja** | 3 | 3 | $\times 10^3$ ($1\text{ k}$) | - |
| **Amarillo** | 4 | 4 | $\times 10^4$ ($10\text{ k}$) | - |
| **Verde** | 5 | 5 | $\times 10^5$ ($100\text{ k}$) | $\pm 0{,}5\%$ |
| **Azul** | 6 | 6 | $\times 10^6$ ($1\text{ M}$) | $\pm 0{,}25\%$ |
| **Violeta** | 7 | 7 | $\times 10^7$ ($10\text{ M}$) | $\pm 0{,}1\%$ |
| **Gris** | 8 | 8 | $\times 10^8$ | - |
| **Blanco** | 9 | 9 | $\times 10^9$ | - |
| **Oro (Dorado)** | - | - | $\times 10^{-1}$ ($0{,}1$) | $\pm 5\%$ |
| **Plata (Plateado)** | - | - | $\times 10^{-2}$ ($0{,}01$) | $\pm 10\%$ |
| **Sin color** | - | - | - | $\pm 20\%$ |

### Fórmula del Valor Nominal:
$$R = (\text{Banda 1} \times 10 + \text{Banda 2}) \times 10^{\text{Banda 3}} \quad [\Omega]$$

### Intervalo de Tolerancia:
$$\Delta R = R_{\text{nom}} \times \frac{\text{Tolerancia}}{100}$$
$$R_{\min} = R_{\text{nom}} - \Delta R \quad ; \quad R_{\max} = R_{\text{nom}} + \Delta R$$

---

## ¿Por qué importa?
1. **Identificación rápida en el laboratorio**: Permite reconocer componentes sin necesidad de recurrir continuamente al polímetro.
2. **Control de calidad y diseño**: La tolerancia indica la precisión del componente; para filtros o temporizadores de precisión como en [[circuito_integrado_555_monoestable_astable]] se requieren tolerancias bajas (marrón $\pm 1\%$ o rojo $\pm 2\%$).

---

## ¿Cómo se aplica o relaciona?
* Aplicado en montaje de placas y protoboard: [[guia_montaje_protoboard_y_seguridad]].
* Enlace con [[resistencias_variables_ldr_ntc_ptc]] y [[asociacion_resistencias]].

### Ejemplo Típico de Examen:
Resistencia con bandas: **Amarillo - Violeta - Rojo - Oro**:
1. 1ª Banda (Amarillo) = $4$
2. 2ª Banda (Violeta) = $7$
3. 3ª Banda (Rojo) = $\times 10^2 = 100$
4. 4ª Banda (Oro) = $\pm 5\%$
* **Valor nominal**: $47 \times 100\,\Omega = 4700\,\Omega = 4{,}7\text{ k}\Omega$.
* **Tolerancia**: $4700 \times 0{,}05 = 235\,\Omega$.
* **Rango admisible**: $[4465\,\Omega \; ; \; 4935\,\Omega]$.
