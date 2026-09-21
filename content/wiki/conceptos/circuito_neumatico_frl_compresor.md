---
title: Circuito Neumático (Generación, FRL y Distribución)
tags: [neumatica, compresor, frl, 3a_evaluacion, 4eso]
aliases: [Unidad de Mantenimiento, FRL, Compresor Neumático, Depósito de Aire]
---

# Circuito Neumático (Generación, FRL y Distribución)

## ¿Qué es?
Un circuito neumático industrial está formado por cuatro etapas secuenciales:
1. **Generación**: Compresor (de émbolo o de tornillo) que aspira aire atmosférico y eleva su presión (típicamente a $6 - 10\text{ bar}$).
2. **Almacenamiento y Seguridad**: Calderín / Depósito de aire con manómetro, válvula limitadora de seguridad y válvula de purga para condensados.
3. **Acondicionamiento (Unidad de Mantenimiento FRL)**.
4. **Distribución y Actuación**: Tuberías, válvulas distribuidoras y cilindros.

### La Unidad de Mantenimiento (FRL):
Es el elemento situado a la entrada de cada máquina o puesto de trabajo neumático para acondicionar el aire comprimido. Integra **tres elementos esenciales**:

1. **Filtro (F)**: Retiene las partículas sólidas de polvo, óxido y separa por centrifugación las gotas de agua condensada que arrastra la corriente de aire, acumulándolas en una purga inferior.
2. **Regulador de Presión (R)**: Mantiene constante la presión de trabajo fijada para el circuito mediante un diafragma y un resorte, independientemente de las fluctuaciones de la red general. Incluye un **manómetro** indicador.
3. **Lubricador (L)**: Inyecta una finísima niebla de aceite mineral en el flujo de aire para lubricar los componentes móviles internos de las válvulas y cilindros, reduciendo la fricción y el desgaste.

```mermaid
graph LR
    COMPRESOR[Compresor de Aire] --> DEPOSITO[Depósito / Acumulador]
    DEPOSITO --> RED[Red de Tuberías con Pendiente]
    RED --> FRL[Unidad FRL: Filtro + Regulador + Lubricador]
    FRL --> VALVULAS[Válvulas de Control]
    VALVULAS --> CILINDROS[Cilindros y Actuadores]
```

---

## ¿Por qué importa?
El aire atmosférico contiene humedad, polvo y contaminantes. Sin una unidad FRL adecuada, los cilindros se oxidarían, las juntas de estanqueidad se degradarían rápidamente y las válvulas quedarían bloqueadas por suciedad.

---

## ¿Cómo se aplica o relaciona?
* Conexión hacia [[valvulas_distribuidoras_neumaticas]] y [[valvulas_logicas_simultaneidad_selectora]].
* Simbología normalizada en [[simbologia_neumatica_y_electronica]].
