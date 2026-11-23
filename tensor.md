# Tensor Cores (5.ª Generación)

[⬅ Volver al inicio](index.md)

## Información General
Los **Tensor Cores** son procesadores especializados diseñados exclusivamente para acelerar la Inteligencia Artificial (IA). La RTX 5060 cuenta con la **5.ª Generación** de estos núcleos, ofreciendo un rendimiento masivo de **614 AI TOPS**. 

![Esquema de Tensor Cores e IA](images/tensor_cores.jpg)

---

## Explicación Detallada
**¿Qué hacen exactamente?**
A diferencia de los Núcleos CUDA que hacen cálculos uno tras otro, los Tensor Cores están diseñados para hacer **operaciones de matrices** (multiplicación y suma de grandes bloques de números) en un solo paso. Esto es el lenguaje nativo de las redes neuronales.

**El impacto en los videojuegos (DLSS 4):**
Su función más famosa es habilitar el **DLSS 4** (Deep Learning Super Sampling). Los Tensor Cores toman una imagen de baja resolución, la analizan mediante IA y la reconstruyen a una resolución 4K u 8K con una calidad casi idéntica al renderizado nativo, multiplicando los FPS.
Además, permiten la **Generación de Fotogramas**: la tarjeta inventa fotogramas intermedios para que el juego se sienta extremadamente fluido.

**En productividad:**
Si usas herramientas como Stable Diffusion (IA generativa), Adobe Premiere o Microsoft Copilot, los Tensor Cores realizan estas tareas hasta 10 veces más rápido que los núcleos tradicionales.