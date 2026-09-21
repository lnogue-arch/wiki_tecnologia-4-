---
title: Guía de Simulación y Prototipado con Autodesk Tinkercad Circuits
tags: [guia, tinkercad, simulacion, arduino, 3a_evaluacion, 4eso]
aliases: [Tinkercad Arduino, Tinkercad Circuits, Simulador Arduino]
---

# Guía de Simulación y Prototipado con Autodesk Tinkercad Circuits

## 1. Acceso y Creación de Proyectos
**Tinkercad Circuits** es una aplicación web gratuita en la nube que permite diseñar esquemas electrónicos, cablear componentes sobre protoboards virtuales y programar placas Arduino simulando su comportamiento físico exacto.

1. Acceder a [tinkercad.com](https://www.tinkercad.com) con la cuenta del centro educativo / clase virtual.
2. Crear un nuevo diseño en la sección **Circuits**.

---

## 2. Flujo de Trabajo en Tinkercad

### Paso 1: Disposición de Componentes
* Arrastra al lienzo de trabajo:
  * 1 Placa **Arduino UNO R3**.
  * 1 **Placa de pruebas pequeña (Protoboard)**.
  * Sensores (LDR, potenciómetros, pulsadores), actuadores (LEDs, servomotores, zumbadores) y resistencias limitadoras.

### Paso 2: Cableado Normalizado por Código de Colores
* **Rojo**: Líneas de alimentación positiva ($+5\text{V}$).
* **Negro**: Líneas de retorno o masa (**GND**).
* **Verde, Azul, Amarillo, Naranja**: Líneas de señal de control y entradas analógicas.

### Paso 3: Programación del Microcontrolador
* Abre el panel **Código** superior.
* Selecciona la modalidad **Texto** (C++ estándar de Arduino).
* Pega o escribe el programa, verifica la sintaxis y pulsa **Iniciar simulación**.

---

## 3. Ventajas para el Aprendizaje
* Permite depurar errores de código y conexionado antes de acudir al taller real.
* Evita la rotura física de placas de Arduino y componentes por inversión de polaridad o sobretensión.

---
*Conceptos relacionados: [[arquitectura_arduino_y_pines]], [[programacion_arduino_funciones_basicas]], [[guia_programacion_arduino_semaforos]].*
