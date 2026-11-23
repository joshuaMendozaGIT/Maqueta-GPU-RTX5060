# Flujo de Trabajo y Procesos

[⬅ Volver al inicio](index.md)

Para entender la arquitectura, es útil seguir el "viaje" de un dato. El proceso se puede dividir en dos grandes vertientes que trabajan en conjunto: el **procesamiento gráfico tradicional** y el **procesamiento de IA**.

## El Viaje de un Dato: Del CPU a la Pantalla

### Fase 1: Preparación y Distribución
1.  **El CPU** envía al GPU los datos de la escena (vértices, texturas, instrucciones) a través del bus **PCIe 5.0**.
2.  Los datos llegan a la **memoria GDDR7**.
3.  El motor de distribución de trabajo (GigaThread Engine) del GPU asigna las tareas a los **GPCs**.

### Fase 2: Procesamiento en los SMs (El núcleo del trabajo)
Dentro de cada SM, los datos fluyen a través de una "tubería" (pipeline) donde intervienen diferentes unidades: [reference:18]

1.  **Vertex Shading (Sombreado de Vértices):** Los **Núcleos CUDA** transforman los modelos 3D (vértices) en coordenadas de pantalla.
2.  **Rasterización (Rasterization):** El **Polymorph Engine** (dentro del TPC) y los **RT Cores** (si el juego usa Ray Tracing) convierten las formas geométricas 3D en píxeles (fragmentos) 2D. [reference:19]
3.  **Pixel Shading (Sombreado de Píxeles):** Los **Núcleos CUDA** calculan el color final de cada píxel, aplicando texturas e iluminación.

### Fase 3: La Intervención de la IA (El diferenciador de Blackwell)
Aquí es donde la arquitectura Blackwell brilla. En lugar de renderizar todos los píxeles a la máxima resolución, el proceso se optimiza:

- **DLSS Super Resolution:** La GPU renderiza la imagen a una resolución menor (por ejemplo, 1080p) y los **Tensor Cores** utilizan IA para reconstruirla a una resolución mayor (4K) con una calidad casi idéntica.
- **Generación de Fotogramas (DLSS 4):** Los Tensor Cores analizan dos fotogramas consecutivos y **generan un fotograma intermedio** completamente nuevo mediante IA. Esto duplica o triplica la tasa de fotogramas (FPS) sin que los Núcleos CUDA tengan que renderizar ese trabajo adicional. [reference:20]
- **Neural Shading:** La IA también puede participar en el sombreado, mejorando la calidad de los materiales y las texturas (RTX Neural Materials). [reference:21]

### Fase 4: Salida
Finalmente, los **ROPs (Raster Operations)** aplican efectos de posprocesamiento (como antialiasing) y envían la imagen final a los controladores de memoria para que se muestre en el monitor a través de los puertos **HDMI 2.1b** o **DisplayPort 2.1b**. [reference:22]