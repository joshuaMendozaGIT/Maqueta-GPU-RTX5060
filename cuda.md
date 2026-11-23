# Núcleos CUDA

[⬅ Volver al inicio](index.md)

## Información General
Los **Núcleos CUDA** son el motor principal de la tarjeta gráfica. La RTX 5060 incorpora un total de **3,840 Núcleos CUDA**, los cuales se encargan de ejecutar los cálculos matemáticos para renderizar los gráficos, procesar la física y realizar tareas de cómputo general.

![Diagrama de un Streaming Multiprocessor](images/diagrama_cuda.jpg) 

---

## Explicación Detallada
**¿Cómo funcionan?**
Cada núcleo CUDA es esencialmente un procesador pequeño que ejecuta instrucciones de forma paralela. En lugar de que un solo procesador muy rápido haga todo el trabajo, miles de núcleos CUDA trabajan simultáneamente, dividiendo la pantalla en miles de píxeles y calculando el color y la luz de cada uno al mismo tiempo.

**Distribución en la arquitectura Blackwell:**
En la RTX 5060, estos 3,840 núcleos no están sueltos; están agrupados en **30 Streaming Multiprocessors (SM)**. Cada uno de estos SM contiene exactamente **128 Núcleos CUDA**. 

**¿Para qué se usan?**
*   **Gráficos 3D:** Sombreado (shading), cálculo de vértices y texturizado.
*   **Cómputo General (GPGPU):** Aceleran tareas en programas de edición de video, renderizado 3D (como Blender) y simulaciones científicas.

**Su papel en el pipeline:** Los Núcleos CUDA son los "obreros" del pipeline gráfico. Ejecutan los *shaders* (programas) de vértices y píxeles. En la arquitectura Blackwell, también pueden ejecutar *shaders neuronales*, trabajando en conjunto con los Tensor Cores para mezclar el renderizado tradicional con el de IA.