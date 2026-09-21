---
title: Referencia de Simbología Normalizada (Electrónica y Neumática ISO 1219)
tags: [assets, simbologia, normas, electronica, neumatica, 4eso]
---

# Referencia de Simbología Normalizada (Electrónica y Neumática ISO 1219)

## 1. Simbología de Electrónica Analógica y Digital

```text
    Resistencia:        --[====]--    o    --/\/\/\--
    Potenciómetro:      --[==/==]--   (con flecha de cursor)
    LDR:                --[====]--    (dos flechas de luz entrantes ->)
    Termistor NTC/PTC:  --[====]--    (-tº o +tº)
    Condensador:        ---| |---     (Electrolítico: ---[| |--- con + y -)
    Diodo estándar:     ---|▷|---     (Ánodo triángulo ▷, Cátodo barra |)
    Diodo LED:          ---|▷|---     (dos flechas de luz salientes ->)
    Transistor NPN:     Colector (arriba), Base (lateral), Emisor (flecha abajo saliente)
    Transistor PNP:     Colector (arriba), Base (lateral), Emisor (flecha entrante hacia base)
    Relé:               -[ [][][] ]- (Bobina) + Contactos COM, NO, NC
```

---

## 2. Simbología de Neumática Industrial (Norma ISO 1219)

### Válvulas Distribuidoras:
```text
  Posición de Reposo / Trabajo (2 cuadros contiguos):
  +-------+-------+
  |  ▲ |  |   | ▲ |   (Flechas indican sentido de flujo de aire)
  |  | |  |   | | |
  +-------+-------+
     1       2
```

* **Vía 1 (P)**: Alimentación de presión (símbolo de triángulo relleno o círculo con punto).
* **Vía 2 / 4 (A / B)**: Salidas de trabajo a cilindros.
* **Vía 3 / 5 (R / S)**: Escapes (triángulo invertido con salida al exterior).

### Elementos de Mando y Accionamiento:
* **Pulsador manual**: Seta o botón mecánico en el lateral de la válvula.
* **Retorno por muelle**: Símbolo en zigzag (*muelle*) en el extremo derecho.
* **Final de carrera por rodillo**: Círculo rodante sobre palanca mecánica.
* **Pilotaje neumático**: Triángulo apuntando hacia la válvula.

### Cilindros:
* **Simple Efecto**: Un pistón con vástago y muelle visible en la cámara delantera.
* **Doble Efecto**: Un pistón con vástago y dos tomas de aire (delantera y trasera), sin muelle.

---
*Conceptos relacionados: [[valvulas_distribuidoras_neumaticas]], [[valvulas_logicas_simultaneidad_selectora]], [[circuito_neumatico_frl_compresor]].*
