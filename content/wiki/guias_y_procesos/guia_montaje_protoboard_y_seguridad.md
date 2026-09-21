---
title: Guía de Montaje en Protoboard y Normas de Seguridad en el Taller
tags: [guia, taller, protoboard, seguridad, electronica, 4eso]
aliases: [Uso Protoboard, Normas de Taller, Cableado Protoboard]
---

# Guía de Montaje en Protoboard y Normas de Seguridad en el Taller

## 1. Estructura Interna de la Placa de Pruebas (Protoboard)

Una protoboard permite interconectar componentes sin necesidad de soldar con estaño:

```text
 (+ RED)  o - o - o - o - o - o - o - o - o - o - o   (Bus Positivo continuo)
 (- BLUE) o - o - o - o - o - o - o - o - o - o - o   (Bus Negativo continuo)
 
   a  b  c  d  e      | CANAL CENTRAL |      f  g  h  i  j
1  o--o--o--o--o      |    AISLANTE   |   1  o--o--o--o--o  (Columnas unidas
2  o--o--o--o--o      |  (Para CIs DIP|   2  o--o--o--o--o   verticalmente
3  o--o--o--o--o      |  como 555, 74)|   3  o--o--o--o--o   de 5 en 5 orificios)
```

1. **Buses Laterales de Alimentación**: Pistas longitudinales continuas (marcadas en rojo para $+V_{cc}$ y azul para GND).
2. **Pistas Centrales de Terminales**: Filas de 5 orificios unidas internamente en sentido transversal.
3. **Canal Central de Aislamiento**: Separa las dos mitades centrales. Está diseñado específicamente para montar **circuitos integrados DIP** (ej. CI 555, puertas 7408) sin que sus patillas opuestas hagan cortocircuito.

---

## 2. Reglas de Oro para un Montaje Limpio y Fiable
1. **Trabajar SIEMPRE sin corriente**: Realizar todo el conexionado con la fuente desconectada o el cable USB desenchufado.
2. **Puentes cortos y rectilíneos**: Evitar bucles de cables aéreos desordenados ("nido de pájaros") que dificultan detectar errores.
3. **Respetar polaridades**:
   * Condensadores electrolíticos (la banda blanca con signo '-' debe ir a GND).
   * Diodos y LEDs (Cátodo a GND).
   * Circuitos integrados (la muesca semicircular o punto guía debe apuntar hacia la izquierda/arriba).
4. **Verificación visual previa**: Revisar minuciosamente los pines de alimentación (Vcc y GND) antes de dar tensión por primera vez.

---
*Conceptos relacionados: [[codigo_colores_resistencias]], [[diodos_y_leds]], [[circuito_integrado_555_monoestable_astable]].*
