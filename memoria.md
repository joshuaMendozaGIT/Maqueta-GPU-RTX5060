# Memoria y Arquitectura

<a href="index.html" style="display: inline-block; padding: 10px 15px; background-color: #0b2e59; color: white; text-decoration: none; border-radius: 5px; font-weight: bold; margin-bottom: 20px;">⬅ Volver al Inicio</a>

<div class="stat-box">
  <h2>448 GB/s</h2>
  <p>Ancho de Banda (8 GB GDDR7)</p>
</div>

<img src="images/memoria_gpu.jpg" alt="Esquema del bus de memoria" class="img-componente">

## Información General
El subsistema de memoria determina la velocidad a la que la GPU puede leer y escribir datos. La RTX 5060 cuenta con **8 GB de memoria GDDR7**, un bus de **128 bits** y un ancho de banda de **448 GB/s**, empaquetado en un diseño térmico de **145 W**.

---

## Explicación Detallada

<details>
  <summary>👉 Haz clic aquí para leer sobre GDDR7, PCIe y Consumo</summary>
  <p style="margin-top: 15px;">
    <strong>Memoria GDDR7 y Ancho de Banda:</strong><br>
    La GDDR7 funciona a <strong>28 Gbps</strong>. Al multiplicar la velocidad por el tamaño del bus (128 bits) y dividirlo entre 8, obtenemos el ancho de banda: <strong>448 GB/s</strong>. Esto significa que la tarjeta puede mover 448 Gigabytes de información por segundo.<br><br>
    <strong>Interfaz PCIe 5.0 x8:</strong><br>
    Configurada eléctricamente en x8 (8 carriles). Es una decisión de diseño para hacer la tarjeta más asequible y eficiente, ya que el PCIe 5.0 x8 ofrece el mismo ancho de banda que un PCIe 4.0 x16, más que suficiente para esta GPU.<br><br>
    <strong>Consumo:</strong><br>
    Su TDP es de <strong>145 W</strong>. No requiere conectores de alimentación masivos y funciona perfectamente con fuentes de alimentación de 550 W.
  </p>
</details>

<details>
  <summary>👉 Haz clic aquí para leer sobre la Caché L2</summary>
  <p style="margin-top: 15px;">
    <strong>La caché L2: El centro de comunicaciones:</strong><br>
    Todos los datos que viajan entre los SMs y la memoria GDDR7 pasan por la <strong>caché L2</strong>. En Blackwell, la L2 es un bloque central masivo. En el caso de la RTX 5060, esta caché es fundamental para mantener a los 30 SMs alimentados con datos, reduciendo la latencia y actuando como un "puente" de alta velocidad entre los distintos GPCs.
  </p>
</details>