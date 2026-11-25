# Evolución de la Arquitectura NVIDIA

<a href="index.html" style="display: inline-block; padding: 10px 15px; background-color: #0b2e59; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; margin-bottom: 20px;">⬅ Volver al Inicio</a>

La RTX 5060 no es un producto aislado; es el resultado de más de una década de evolución. Cada generación de arquitectura NVIDIA introdujo innovaciones clave que, acumuladas, dan forma a la GPU que estudiamos.

## Línea de Tiempo de las Arquitecturas Clave

| Año | Arquitectura | Hito Principal |
| :--- | :--- | :--- |
| **2018** | **Turing** | Introdujo los **primeros RT Cores** y los **Tensor Cores de 2.ª generación**. Se añadió la caché unificada por primera vez. [reference:0] |
| **2020** | **Ampere** | Duplicó el rendimiento de FP32, introdujo los **Tensor Cores de 3.ª generación** (con soporte para TF32 y BF16) y una **gran caché L2**. [reference:1][reference:2] |
| **2022** | **Ada Lovelace** | Llevó los **RT Cores de 3.ª generación** y los **Tensor Cores de 4.ª generación** (con soporte para **FP8**), habilitando el **DLSS 3** con generación de fotogramas. [reference:3][reference:4] |
| **2025** | **Blackwell** | La arquitectura de la RTX 5060. Introduce los **Tensor Cores de 5.ª generación** con soporte nativo para **FP4 y FP6**, y los **RT Cores de 4.ª generación**. Está optimizada para el **DLSS 4** y el **renderizado neuronal**. [reference:5][reference:6] |

## ¿Qué hace especial a Blackwell?

La RTX 5060 hereda lo mejor de sus predecesoras, pero su gran salto está en la **integración de la IA en el proceso de renderizado**. Mientras que en generaciones anteriores la IA se usaba principalmente para el reescalado (DLSS), en Blackwell la IA participa en la propia generación de geometría y texturas (Neural Shading). [reference:7][reference:8]

Además, sus Tensor Cores de 5.ª generación son los primeros en soportar de forma nativa el formato **FP4** (coma flotante de 4 bits). Esto duplica la velocidad de procesamiento para IA en comparación con FP8, manteniendo una precisión aceptable para muchas tareas, lo que es clave para el DLSS 4 y las aplicaciones de IA generativa. [reference:9][reference:10][reference:11]