# Jerarquía Interna de la GPU

<a href="index.html" style="display: inline-block; padding: 10px 15px; background-color: #0b2e59; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; margin-bottom: 20px;">⬅ Volver al Inicio</a>

<div class="stat-box">
  <h2>3 Niveles</h2>
  <p>GPC ➔ TPC ➔ SM (30 SMs en total)</p>
</div>

<img src="assets/images/jerarquia_gpu.jpg" alt="Jerarquía de la GPU" class="img-componente">

## Información General
Una GPU no es un solo bloque monolítico. Para manejar miles de millones de operaciones por segundo, sus componentes se organizan en una jerarquía estricta que optimiza la comunicación y el reparto de trabajo. En la RTX 5060, esta organización se divide en tres niveles principales: **GPC**, **TPC** y **SM**.

---

## Explicación Detallada

<details>
  <summary>👉 Haz clic aquí para entender el nivel 1: GPC (Graphics Processing Cluster)</summary>
  <p style="margin-top: 15px;">
    Es el nivel más alto de la jerarquía. Un GPC es una unidad autónoma que contiene todos los recursos necesarios para procesar un conjunto de tareas gráficas.<br><br>
    <strong>Función:</strong> Agrupa varios TPCs y se encarga de tareas como la rasterización y la generación de píxeles. La RTX 5060 basada en el chip GB206 contiene un total de <strong>3 GPCs</strong>.
  </p>
</details>

<details>
  <summary>👉 Haz clic aquí para entender el nivel 2: TPC (Texture Processing Cluster)</summary>
  <p style="margin-top: 15px;">
    Es el nivel intermedio. Un TPC agrupa varios SMs junto con unidades de textura y una caché de instrucciones compartida.<br><br>
    <strong>Función:</strong> Actúa como un nodo de interconexión y comparte recursos (como la caché de texturas) entre los SMs que contiene. La RTX 5060 tiene un total de <strong>18 TPCs</strong>.
  </p>
</details>

<details>
  <summary>👉 Haz clic aquí para entender el nivel 3: SM (Streaming Multiprocessor)</summary>
  <p style="margin-top: 15px;">
    Es la <strong>unidad fundamental de cómputo</strong>. Aquí es donde ocurre el trabajo real. Cada SM es un procesador completo por sí mismo.<br><br>
    <strong>Composición en Blackwell:</strong> Cada SM contiene <strong>128 Núcleos CUDA</strong> (organizados en 4 bloques de 32), <strong>4 Tensor Cores</strong> de 5.ª generación, <strong>1 RT Core</strong> de 4.ª generación, así como unidades de textura (TMU), planificadores de warps y una caché L1/Shared Memory unificada de 256 KB.
  </p>
</details>

> **En resumen:** La RTX 5060 tiene **30 SMs**. Estos se agrupan en **18 TPCs** (algunos TPCs tienen 1 SM y otros 2). Y estos 18 TPCs se distribuyen en **3 GPCs**.