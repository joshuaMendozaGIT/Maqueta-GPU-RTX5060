# RT Cores (4.ª Generación)

<a href="index.html" style="display: inline-block; padding: 10px 15px; background-color: #0b2e59; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; margin-bottom: 20px;">⬅ Volver al Inicio</a>

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

**RT Cores de 4.ª Generación y Mega Geometry:** Los RT Cores de la RTX 5060 no solo calculan la intersección de rayos con triángulos. La arquitectura Blackwell introduce **Mega Geometry**, una tecnología que permite a los RT Cores manejar escenas con una cantidad masiva de geometría (como los micromodelos de *Unreal Engine 5 Nanite*), acelerando el trazado de rayos en escenas complejas sin penalizar el rendimiento. [reference:25][reference:26]