# Memoria y Arquitectura

[⬅ Volver al inicio](index.md)

## Información General
El subsistema de memoria determina la velocidad a la que la GPU puede leer y escribir datos. La RTX 5060 cuenta con **8 GB de memoria GDDR7**, un bus de **128 bits** y un ancho de banda de **448 GB/s**, empaquetado en un diseño térmico de **145 W**.

![Esquema del bus de memoria](images/memoria_gpu.jpg)

---

## Explicación Detallada
**Memoria GDDR7 y Ancho de Banda:**
La GDDR7 es la tecnología de memoria gráfica más avanzada. Funciona a **28 Gbps** (Gigabits por segundo). Al multiplicar la velocidad por el tamaño del bus (128 bits) y dividirlo entre 8, obtenemos el ancho de banda: **448 GB/s**. Esto significa que la tarjeta puede mover 448 Gigabytes de información por segundo.

**Interfaz PCIe 5.0 x8:**
La tarjeta utiliza la interfaz PCI Express 5.0, pero configurada eléctricamente en x8 (8 carriles). Esto es una decisión de diseño de NVIDIA para hacer la tarjeta más asequible y eficiente, ya que el PCIe 5.0 x8 ofrece el mismo ancho de banda que un PCIe 4.0 x16, más que suficiente para esta GPU.

**Consumo:**
Su TDP (Thermal Design Power) es de **145 W**. Esto significa que no requiere conectores de alimentación masivos y puede funcionar perfectamente con fuentes de alimentación de 550 W, lo que la hace ideal para actualizar computadoras sin cambiar la fuente.