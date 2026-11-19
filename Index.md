# Arquitectura de la GPU NVIDIA RTX 5060

Bienvenido a la documentación técnica de la maqueta sobre la **NVIDIA GeForce RTX 5060**, una tarjeta gráfica basada en la arquitectura **Blackwell 2.0** de NVIDIA. Esta página reúne la información esencial para entender cómo está construida la GPU, desde sus bloques funcionales hasta su configuración de memoria.

La RTX 5060 está fabricada por **TSMC en un proceso de 5 nm (4N FinFET)** e integra el chip gráfico **GB206-250-A1**. Su diseño se organiza en torno a **30 Streaming Multiprocessors (SM)**, que son la unidad fundamental de cómputo de la arquitectura Blackwell.[reference:0]

---

## Bloques funcionales principales

Cada uno de los 30 SM de la RTX 5060 contiene un conjunto fijo de unidades especializadas. Esta es la configuración exacta de la versión de escritorio:

| Componente | Cantidad total | Distribución por SM |
| :--- | :--- | :--- |
| **Núcleos CUDA** | 3,840 | 128 por SM |
| **Tensor Cores (5.ª gen)** | 120 | 4 por SM |
| **RT Cores (4.ª gen)** | 30 | 1 por SM |
| **TMUs** | 120 | — |
| **ROPs** | 48 | — |

Los **núcleos CUDA** se encargan del sombreado y el cómputo general. Los **Tensor Cores de 5.ª generación** aceleran cargas de inteligencia artificial y tecnologías como DLSS 4, mientras que los **RT Cores de 4.ª generación** están dedicados al trazado de rayos en tiempo real. La GPU alcanza **614 AI TOPS** en rendimiento de inteligencia artificial.[reference:1]

---

## Memoria y conexión

La RTX 5060 incorpora **8 GB de memoria GDDR7** en un bus de **128 bits**. La memoria funciona a **28 Gbps efectivos**, lo que produce un **ancho de banda de 448 GB/s**. Utiliza una interfaz **PCIe 5.0 ×8** y ofrece salidas **HDMI 2.1b** y **DisplayPort 2.1b**.[reference:2][reference:3]

| Especificación | Valor |
| :--- | :--- |
| Memoria | 8 GB GDDR7 |
| Bus de memoria | 128 bits |
| Ancho de banda | 448 GB/s |
| Interfaz | PCIe 5.0 ×8 |
| TDP (referencia) | 150 W (145 W en modelos personalizados) |

> **Nota sobre el TDP:** El valor de referencia de NVIDIA es de **150 W**, aunque muchos ensambladores (ASUS, Gigabyte, Palit, etc.) comercializan modelos con un TDP configurado en **145 W**.[reference:4][reference:5]

---

## Una arquitectura que se adapta: escritorio vs. portátil

La misma base Blackwell se utiliza en la **RTX 5060 para portátil**, pero con una configuración de núcleos reducida para adaptarse a las limitaciones de energía y refrigeración de los equipos móviles. Esta es la diferencia técnica más importante entre ambas versiones:

| Especificación | RTX 5060 (escritorio) | RTX 5060 (portátil) |
| :--- | :--- | :--- |
| **Núcleos CUDA** | **3,840** | **3,328** |
| **Diferencia** | — | **~13–15 % menos** |
| **TDP / TGP** | ~145–150 W | 45–100 W (+ Dynamic Boost) |

La versión de portátil también reduce la cantidad de RT Cores y Tensor Cores de forma proporcional. Esta diferencia es un ejemplo de cómo una misma arquitectura se ajusta a distintos formatos sin perder su identidad técnica.[reference:6]

---

## Explora la documentación

- **[Especificaciones detalladas](especificaciones.md)** — Tabla completa de especificaciones técnicas.
- **[Referencias](referencias.md)** — Fuentes y enlaces para validar la información.

---

*Página creada para la maqueta de arquitectura de la GPU RTX 5060. La información técnica se basa en especificaciones públicas de NVIDIA y análisis de medios especializados.*