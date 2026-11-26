# Arquitectura de la GPU NVIDIA RTX 5060 (8 GB GDDR7)

<!-- PORTADA DE BIENVENIDA -->
<!-- PORTADA DE BIENVENIDA AUTOMÁTICA (Solo primera visita) -->
<div id="splash-screen">
  <img src="assets/images/logo-tecnm.png" alt="TecNM" class="splash-logo">
</div>

<script>
  // Verificamos si el usuario ya vio la portada en esta sesión
  if (sessionStorage.getItem('splashVisto') !== 'true') {
    // Si es la primera vez, mostramos el logo y esperamos 2.5 segundos
    setTimeout(function() {
      var splash = document.getElementById('splash-screen');
      if (splash) {
        splash.style.opacity = '0'; // Inicia el desvanecimiento
        setTimeout(function() {
          splash.style.display = 'none'; // Lo oculta por completo
        }, 1000); // Espera a que termine la transición de CSS (1 segundo)
      }
    }, 2500); 
    
    // Marcamos que ya se vio la portada
    sessionStorage.setItem('splashVisto', 'true');
  } else {
    // Si ya la vio, la ocultamos de inmediato sin mostrar nada
    document.getElementById('splash-screen').style.display = 'none';
  }
</script>
<!-- FIN DE LA PORTADA -->

<div class="logos-bar">
  <img src="assets/images/logo-tecnm.png" alt="TecNM">
  <img src="assets/images/logo-itcelaya.png" alt="ITCelaya">
</div>

<div class="hero">
<!-- FIN DE LA PORTADA -->

<div class="logos-bar">
  <img src="assets/images/logo-tecnm.png" alt="TecNM">
  <img src="assets/images/logo-itcelaya.png" alt="ITCelaya">
</div>

<div class="hero">

<div class="logos-bar">
  <img src="assets/images/logo-tecnm.png" alt="TecNM">
  <img src="assets/images/logo-itcelaya.png" alt="ITCelaya">
</div>

<div class="hero">
  <h1>Arquitectura de la GPU NVIDIA RTX 5060</h1>
  <p>Proyecto de Maqueta y Documentación Técnica - Arquitectura de Computadoras</p>
  <img class="gpu-img" src="assets/images/gpu-hero.jpg" alt="NVIDIA RTX 5060">
</div>

## Resumen del Proyecto

Bienvenido a la plataforma interactiva de la maqueta sobre la **NVIDIA GeForce RTX 5060**, basada en la arquitectura **NVIDIA Blackwell**. Esta documentación ha sido diseñada para complementar el modelo físico, permitiendo a los usuarios escanear los códigos QR y explorar el detalle técnico de cada componente.

<div class="grid-container">

  <a href="cuda.html" class="card">
    <h3>🧠 Núcleos CUDA</h3>
    <p>El motor principal del procesamiento gráfico. Descubre cómo operan los 3,840 núcleos de la RTX 5060.</p>
  </a>

  <a href="tensor.html" class="card">
    <h3>🤖 Tensor Cores</h3>
    <p>La potencia detrás de la inteligencia artificial, el DLSS 4 y el rendimiento de 614 AI TOPS.</p>
  </a>

  <a href="rt.html" class="card">
    <h3>💡 RT Cores</h3>
    <p>El hardware dedicado al trazado de rayos en tiempo real y la tecnología Mega Geometry.</p>
  </a>

  <a href="memoria.html" class="card">
    <h3>⚡ Memoria y Conexión</h3>
    <p>El subsistema de memoria GDDR7, el ancho de banda de 448 GB/s y la interfaz PCIe 5.0.</p>
  </a>

  <a href="jerarquia.html" class="card">
    <h3>🏗️ Jerarquía Interna</h3>
    <p>Cómo se organizan los componentes internamente: GPC, TPC y los 30 SMs de la tarjeta.</p>
  </a>

  <a href="flujo-trabajo.html" class="card">
    <h3>🔄 Flujo de Trabajo</h3>
    <p>El viaje de un dato: desde que el CPU envía la instrucción hasta la renderización en pantalla.</p>
  </a>

  <a href="evolucion.html" class="card">
    <h3>🕰️ Evolución Histórica</h3>
    <p>El camino de NVIDIA desde Turing hasta Blackwell y cómo llegamos a esta arquitectura.</p>
  </a>

</div>

<br>
<div style="text-align: center; font-size: 0.9em; color: #666; margin-top: 40px;">
  <p><strong>Tecnológico Nacional de México - Campus Celaya</strong><br>
  Departamento de Sistemas y Computación</p>
</div>