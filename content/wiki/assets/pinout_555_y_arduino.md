---
title: Diagramas de Pines (Pinouts) del CI 555 y Arduino UNO
tags: [assets, pinout, ci_555, arduino, hardware, 4eso]
---

# Diagramas de Pines (Pinouts) del CI 555 y Arduino UNO

## 1. Pinout del Temporizador NE555 (Cápsula DIP-8)

```text
              +-------+--+-------+
       GND -- | 1 (GND)    8 (Vcc)| -- Vcc (+5V a +15V)
   TRIGGER -- | 2 (TRIG)   7 (DIS)| -- DISCHARGE (Descarga)
    OUTPUT -- | 3 (OUT)    6 (THR)| -- THRESHOLD (Umbral)
     RESET -- | 4 (RES)    5 (CON)| -- CONTROL VOLTAGE
              +------------------+
```

| Nº Pin | Nombre | Función |
| :---: | :--- | :--- |
| **1** | **GND** | Masa o polo negativo ($0\text{ V}$). |
| **2** | **TRIGGER** | Disparo: inicia la temporización si el voltaje cae por debajo de $\frac{1}{3}V_{cc}$. |
| **3** | **OUTPUT** | Salida: nivel alto ($V_{cc} - 1{,}5\text{ V}$) o bajo ($0\text{ V}$). |
| **4** | **RESET** | Reinicio activo a nivel bajo (conectar a Vcc si no se usa). |
| **5** | **CONTROL** | Modificación del umbral interno (filtrar a GND con $10\text{ nF}$). |
| **6** | **THRESHOLD**| Umbral: finaliza la temporización si el voltaje supera $\frac{2}{3}V_{cc}$. |
| **7** | **DISCHARGE**| Descarga: transistor interno conectado a masa para descargar el condensador $C$. |
| **8** | **Vcc** | Alimentación positiva ($+4{,}5\text{ V}$ a $+15\text{ V}$). |

---

## 2. Mapa de Pines de Arduino UNO R3

```text
                               +-------------------+
                               | USB   [ATmega16U2]|
                               | PORT              |
                          +----+                   +----+
             [RESET] ---- | IOREF                 D13/SCK | ---- [LED 'L' Integrado]
                          | RESET             (~) D12/MISO|
                   +5V -- | 3.3V              (~) D11/MOSI| ~ PWM
                  GND --- | 5V                (~) D10/SS  | ~ PWM
                  GND --- | GND               (~) D9      | ~ PWM
            Vin (7-12V) - | GND                   D8      |
                          | Vin                           |
                          |                       D7      |
        [Sensor A0] ----- | A0                (~) D6      | ~ PWM
        [Sensor A1] ----- | A1                (~) D5      | ~ PWM
        [Sensor A2] ----- | A2                    D4      |
        [Sensor A3] ----- | A3                (~) D3      | ~ PWM / INT1
   [SDA I2C] ------------ | A4                    D2      | [Interrupción 0]
   [SCL I2C] ------------ | A5                    D1 (TX) | ---> Transmisión Serie
                          +-----------------------D0 (RX)-+ <--- Recepción Serie
                                     [ ATmega328P ]
```

---
*Conceptos relacionados: [[circuito_integrado_555_monoestable_astable]], [[arquitectura_arduino_y_pines]].*
