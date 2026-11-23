# RT Cores (4.ª Generación)

[⬅ Volver al inicio](index.md)

## Información General
Los **RT Cores** (Ray Tracing Cores) son unidades de hardware dedicadas exclusivamente a calcular el trazado de rayos en tiempo real. La RTX 5060 equipa la **4.ª Generación** de estos núcleos, alcanzando una potencia de **58 TFLOPS**.

![Ilustración de Trazado de Rayos](images/rt_cores.jpg)

---

## Explicación Detallada
**¿Qué es el Ray Tracing?**
El trazado de rayos es una técnica de renderizado que simula el comportamiento físico real de la luz. Se lanzan "rayos" virtuales desde la cámara hacia la escena para calcular cómo rebotan en los objetos.

**El problema del hardware tradicional:**
Hacer esto con Núcleos CUDA tradicionales requiere una cantidad enorme de cálculos, lo que haría que los juegos corrieran a muy pocos FPS (fotogramas por segundo).

**La solución de los RT Cores:**
Los RT Cores tienen la capacidad de calcular intersecciones de rayos con triángulos (la base de los modelos 3D) de forma ultrarrápida. Esto permite que juegos como *Cyberpunk 2077* o *Alan Wake 2* tengan reflejos precisos en el agua, sombras realistas y refracciones de luz sin que la tarjeta colapse, trabajando en conjunto con los Tensor Cores (DLSS) para mantener la fluidez.