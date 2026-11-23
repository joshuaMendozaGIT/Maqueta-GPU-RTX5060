# Jerarquía Interna de la GPU

[⬅ Volver al inicio](index.md)

Una GPU no es un solo bloque monolítico. Para manejar miles de millones de operaciones por segundo, sus componentes se organizan en una jerarquía estricta que optimiza la comunicación y el reparto de trabajo. En la RTX 5060, esta organización se divide en tres niveles principales: **GPC**, **TPC** y **SM**.

## El Organigrama de la RTX 5060

La RTX 5060, basada en el chip GB206, contiene un total de **3 GPCs**, que agrupan **18 TPCs** y un total de **30 SMs**. [reference:12]

### 1. GPC (Graphics Processing Cluster / Clúster de Procesamiento Gráfico)
Es el nivel más alto de la jerarquía. Un GPC es una unidad autónoma que contiene todos los recursos necesarios para procesar un conjunto de tareas gráficas. 
- **Función:** Agrupa varios TPCs y se encarga de tareas como la rasterización y la generación de píxeles. [reference:13]

### 2. TPC (Texture Processing Cluster / Clúster de Procesamiento de Texturas)
Es el nivel intermedio. Un TPC agrupa varios SMs junto con unidades de textura y una caché de instrucciones compartida.
- **Función:** Actúa como un nodo de interconexión y comparte recursos (como la caché de texturas) entre los SMs que contiene. [reference:14][reference:15]

### 3. SM (Streaming Multiprocessor / Multiprocesador de Flujo)
Es la **unidad fundamental de cómputo**. Aquí es donde ocurre el trabajo real. Cada SM es un procesador completo por sí mismo.
- **Composición (en Blackwell):** Cada SM contiene **128 Núcleos CUDA** (organizados en 4 bloques de 32), **4 Tensor Cores** de 5.ª generación, **1 RT Core** de 4.ª generación, así como unidades de textura (TMU), planificadores de warps y una caché L1/Shared Memory unificada de 256 KB. [reference:16]

---
**En resumen:** La RTX 5060 tiene **30 SMs**. Estos se agrupan en **18 TPCs** (algunos TPCs tienen 1 SM y otros 2). Y estos 18 TPCs se distribuyen en **3 GPCs**. [reference:17]