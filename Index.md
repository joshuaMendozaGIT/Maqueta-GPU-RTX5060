# Arquitectura de la GPU NVIDIA RTX 5060

La **RTX 5060** es una tarjeta gráfica basada en la arquitectura **NVIDIA Blackwell**, la misma generación que da forma a las GPU de escritorio y portátiles de la serie RTX 50. Está fabricada por **TSMC en un proceso de 4NP (5 nm)** e integra el chip gráfico **GB206**[reference:7].

## Bloques funcionales principales

La arquitectura se organiza en torno a **30 Streaming Multiprocessors (SM)**. Cada SM contiene:

- **128 núcleos CUDA**, encargados del sombreado y el cómputo general. En total, la GPU reúne **3,840 núcleos CUDA**[reference:8].
- **4 Tensor Cores de 5.ª generación**, diseñados para acelerar cargas de inteligencia artificial y tecnologías como DLSS. En conjunto suman **120 Tensor Cores**[reference:9].
- **1 RT Core de 4.ª generación**, dedicado al trazado de rayos en tiempo real. En total, **30 RT Cores**[reference:10].

## Memoria y conexión

La RTX 5060 incorpora **8 GB de memoria GDDR7** en un bus de **128 bits**, con un ancho de banda de **448 GB/s**. Utiliza una interfaz **PCIe 5.0 ×8** y ofrece salidas **HDMI 2.1b** y **DisplayPort 2.1b**[reference:11].

## Una arquitectura que se adapta

La misma base Blackwell se utiliza en la **RTX 5060 para portátil**, aunque con **3,328 núcleos CUDA** en lugar de 3,840. Esta reducción responde a las limitaciones de energía y refrigeración de los equipos portátiles, y es un ejemplo de cómo una arquitectura se ajusta a distintos formatos sin perder su identidad técnica.