# Núcleos CUDA

<a href="index.html" style="display: inline-block; padding: 10px 15px; background-color: #0b2e59; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; margin-bottom: 20px;">⬅ Volver al Inicio</a>

<div class="stat-box">
  <h2>3,840</h2>
  <p>Núcleos CUDA en total</p>
</div>

<img src="images/diagrama_cuda.jpg" alt="Diagrama de un Streaming Multiprocessor" class="img-componente"> 

## Información General
Los **Núcleos CUDA** son el motor principal de la tarjeta gráfica. La RTX 5060 incorpora un total de **3,840 Núcleos CUDA**, los cuales se encargan de ejecutar los cálculos matemáticos para renderizar los gráficos, procesar la física y realizar tareas de cómputo general.

---

## Explicación Detallada

<details>
  <summary>👉 Haz clic aquí para leer sobre su funcionamiento y distribución</summary>
  <p style="margin-top: 15px;">
    <strong>¿Cómo funcionan?</strong><br>
    Cada núcleo CUDA es esencialmente un procesador pequeño que ejecuta instrucciones de forma paralela. En lugar de que un solo procesador muy rápido haga todo el trabajo, miles de núcleos CUDA trabajan simultáneamente, dividiendo la pantalla en miles de píxeles y calculando el color y la luz de cada uno al mismo tiempo.<br><br>
    <strong>Distribución en la arquitectura Blackwell:</strong><br>
    En la RTX 5060, estos 3,840 núcleos no están sueltos; están agrupados en <strong>30 Streaming Multiprocessors (SM)</strong>. Cada uno de estos SM contiene exactamente <strong>128 Núcleos CUDA</strong>.
  </p>
</details>

<details>
  <summary>👉 Haz clic aquí para leer sobre sus usos y el pipeline</summary>
  <p style="margin-top: 15px;">
    <strong>¿Para qué se usan?</strong><br>
    *   <strong>Gráficos 3D:</strong> Sombreado (shading), cálculo de vértices y texturizado.<br>
    *   <strong>Cómputo General (GPGPU):</strong> Aceleran tareas en programas de edición de video, renderizado 3D (como Blender) y simulaciones científicas.<br><br>
    <strong>Su papel en el pipeline:</strong><br>
    Los Núcleos CUDA son los "obreros" del pipeline gráfico. Ejecutan los <i>shaders</i> (programas) de vértices y píxeles. En la arquitectura Blackwell, también pueden ejecutar <i>shaders neuronales</i>, trabajando en conjunto con los Tensor Cores para mezclar el renderizado tradicional con el de IA.
  </p>
</details>