# Referencias Técnicas

[⬅ Volver al inicio](index.md)

Esta página reúne las fuentes consultadas para validar las especificaciones y los conceptos arquitectónicos de la GeForce RTX 5060 (8 GB) que aparecen en la documentación de la maqueta.

---

## Especificaciones Oficiales de la RTX 5060

*   **TechPowerUp — Base de datos de GPU (GIGABYTE RTX 5060 WINDFORCE OC):** Fuente principal para el desglose técnico del chip GB206-250-A1, los 30 SM, los 3,840 núcleos CUDA, los 120 Tensor Cores, los 30 RT Cores, la memoria GDDR7 de 8 GB, el bus de 128 bits, el ancho de banda de 448 GB/s y el TDP de 145 W. También detalla la caché L2 de 32 MB y los formatos de datos matriciales soportados (FP4, FP6, FP8, INT8, etc.)[reference:0].
    *   https://www.techpowerup.com/gpu-specs/gigabyte-rtx-5060-windforce-oc.b12580

*   **Profesional Review — "Nvidia RTX 5060 lanzada oficialmente… ¿8GB es suficiente en 2025?" (19 de mayo de 2025):** Artículo de lanzamiento que confirma la arquitectura Blackwell, el proceso de 5 nm (4N), el chip GB206, la configuración de 30 SM, 3,840 CUDA, 120 Tensor Cores de 5.ª generación, 30 RT Cores de 4.ª generación, 120 TMUs, 48 ROPs y 614 AI TOPS. También menciona la interfaz PCIe 5.0 y las salidas de video[reference:1].
    *   https://www.profesionalreview.com/2025/05/19/nvidia-rtx-5060/

---

## Jerarquía Interna y Arquitectura Blackwell

*   **NVIDIA — Guía de Arquitectura Blackwell (Documentación para Desarrolladores):** Documentación oficial que describe la jerarquía de los componentes: los **GPC (Graphics Processing Clusters)** que agrupan **TPC (Texture Processing Clusters)**, los cuales a su vez contienen los **SM (Streaming Multiprocessors)**. También detalla que cada SM de Blackwell tiene 128 núcleos CUDA y que los pares de SM comparten una caché L1 de 256 KiB[reference:2].
    *   https://developer.download.nvidia.cn/assets/embedded/secure/jetson/thor/docs/Thor-Soc-TRM_DP-11881-002_v1.1.pdf (Documento técnico de NVIDIA)

*   **Cornell Virtual Workshop — "Horizon GPUs: Blackwell B200":** Explica la organización jerárquica de la arquitectura Blackwell, confirmando que los SM se emparejan en TPC y que estos se agrupan en GPC. Es una fuente académica que valida la estructura organizativa de la GPU[reference:3].
    *   https://cvw.cac.cornell.edu/gpu-architecture/horizon-gpus-blackwell-b200/blackwell_chip

---

## DLSS 4, Tensor Cores de 5.ª Generación y FP4

*   **Profesional Review — "NVIDIA saca pecho de Blackwell RTX por su promesa en gaming y renderizado neuronal" (26 de agosto de 2025):** Artículo que detalla las innovaciones de Blackwell: los **Tensor Cores de 5.ª generación con soporte para FP4**, la tecnología **DLSS 4** (que puede generar el 100% de los píxeles después del primer fotograma) y los **RT Cores de 4.ª generación**. También menciona el **AI Management Processor (AMP)** para gestionar cargas de IA y gráficos simultáneamente[reference:4].
    *   https://www.profesionalreview.com/2025/08/26/nvidia-saca-pecho-de-blackwell-rtx-por-su-promesa-en-gaming-y-renderizado-neuronal/amp/

*   **GameGPU — "NVIDIA mostró las innovaciones clave de Blackwell RTX: DLSS 4, Tensor Cores de 5.ª generación y un avance en renderizado neuronal":** Fuente técnica que confirma que los Tensor Cores de 5.ª generación ofrecen **hasta 4000 AI TOPS** en las GPU de gama alta y que soportan **FP4**. Explica que DLSS 4 utiliza **Multi Frame Generation (MFG)** para generar fotogramas completos mediante IA[reference:5].
    *   https://gamegpu.com/железо/nvidia-pokazala-klyuchevye-innovatsii-blackwell-rtx-dlss-4-5-e-pokolenie-tensor-cores-i-proryv-v-nejronnom-renderinge

---

## RTX Mega Geometry y RT Cores de 4.ª Generación

*   **PCCentral — "Nvidia RTX Mega Geometry Announced at GDC 2026 for Gaming":** Reporte técnico que explica que las GPU Blackwell de la serie RTX 50 incluyen **motores de hardware dedicados para la intersección y compresión de clústeres de triángulos**, lo que permite acelerar **RTX Mega Geometry**. Indica que la tasa de intersección rayo-triángulo se **duplica** en comparación con los RT Cores de 3.ª generación[reference:6].
    *   https://pccentral.net/nvidia-rtx-mega-geometry-announced-gdc-2026/

*   **Fanáticos del Hardware — "NVIDIA muestra RTX Mega Geometry en GDC 2026 con demos en Alan Wake 2 y The Witcher 4":** Artículo que detalla el funcionamiento de **RTX Mega Geometry**: utiliza un sistema de **clústeres de triángulos anidados** para reorganizar la geometría, reduciendo el coste computacional de las intersecciones de rayos y el uso de VRAM. Menciona que los **RT Cores de las RTX 50 están preparados a nivel de hardware** para esta tecnología, con mejoras de rendimiento de entre el 5% y el 20% en escenas con path tracing[reference:7].
    *   https://fanaticosdelhardware.com/nvidia-muestra-rtx-mega-geometry-en-gdc-2026-con-demos-en-alan-wake-2-y-the-witcher-4/

---

## Evolución Histórica de las Arquitecturas NVIDIA

*   **The CUDA Handbook — "2.6 GPU Architecture":** Referencia académica que resume la evolución de las arquitecturas CUDA-capaces, desde Tesla (2006) hasta Blackwell (2025). Confirma los hitos clave:
    *   **Turing (2018):** Introdujo los **RT Cores de primera generación** y los **Tensor Cores de segunda generación**[reference:8].
    *   **Ampere (2020):** Duplicó el rendimiento de FP32 e introdujo una **gran caché L2**[reference:9].
    *   **Ada Lovelace (2022):** Contemporánea de consumo de Hopper, con Tensor Cores de 4.ª generación y soporte para **FP8**[reference:10].
    *   **Blackwell (2025):** Introduce los **Tensor Cores con soporte para FP4** y la integración de INT32 en las líneas de FP32[reference:11].
    *   https://www.cudahandbook.com/book/ch2/gpu-architecture

*   **Digit — "NVIDIA Blackwell: Here’s everything you need to know":** Artículo de divulgación técnica que contextualiza la evolución: Turing introdujo el hardware dedicado para ray tracing e IA; Ampere refinó el modelo con RT Cores de 2.ª generación y Tensor Cores de 3.ª generación; Ada Lovelace añadió densidad computacional y DLSS 3; y **Blackwell** se centra en el **renderizado neuronal**, los **RTX Neural Shaders** y un diseño basado en **chiplets**[reference:12].
    *   https://www.digit.in/features/gaming/nvidia-blackwell-heres-everything-you-need-to-know.html/amp/

---

*Nota: Las especificaciones exactas de relojes y TDP pueden variar ligeramente entre los distintos modelos de ensambladores (ASUS, Gigabyte, MSI, etc.). Para la maqueta se han utilizado los valores de referencia del modelo base de 8 GB.*