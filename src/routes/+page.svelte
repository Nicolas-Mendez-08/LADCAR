<script>
  // WhatsApp
  const whatsappNumber = "52XXXXXXXXXX";
  const whatsappMessage = encodeURIComponent("Quiero mi promoción");
  const whatsappLink = `https://wa.me/${whatsappNumber}?text=${whatsappMessage}`;

  // Menú de navegación
  const nav = [
    { id: "inicio", icon: "🏠", label: "Inicio" },
    { id: "ladcar", icon: "⭐", label: "¿Por qué LADCAR?" },
    { id: "promocion", icon: "🎁", label: "Promoción" },
    { id: "ubicacion", icon: "📍", label: "Ubicación" },
    { id: "contacto", icon: "✅", label: "Contacto" },
  ];
  function scrollToSection(id) {
    const el = document.getElementById(id);
    if (el) el.scrollIntoView({ behavior: "smooth", block: "start" });
  }
</script>

<!-- MENÚ DE ICONOS FLOTANTE -->
<div class="fixed left-4 top-1/2 -translate-y-1/2 z-50 flex flex-col gap-6">
  {#each nav as item}
    <button
      class="group backdrop-blur-md bg-white/10 hover:bg-red-700/50 text-white border border-white/10 shadow-xl rounded-xl p-3 transition flex flex-col items-center"

      aria-label={item.label}
      on:click={() => scrollToSection(item.id)}
      tabindex="0"
    >
      <span class="text-2xl">{item.icon}</span>
      <span class="absolute left-12 opacity-0 group-hover:opacity-100 transition bg-black text-white px-2 py-1 rounded shadow text-xs pointer-events-none">
        {item.label}
      </span>
    </button>
  {/each}
</div>

<!-- BOTÓN WHATSAPP FLOTANTE -->
<a href={whatsappLink} target="_blank" rel="noopener"
  class="fixed bottom-6 right-6 z-50 flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-bold px-5 py-3 rounded-full shadow-xl text-lg transition-all ring-2 ring-white">
  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
    stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
    d="M16.72 12.06c-.26-.13-1.54-.76-1.77-.85-.24-.08-.41-.13-.58.13-.17.25-.67.85-.83 1.02-.15.17-.31.19-.57.06-.26-.13-1.09-.4-2.08-1.29-.77-.69-1.29-1.54-1.44-1.8-.15-.26-.02-.4.11-.53.11-.11.25-.29.37-.44.12-.15.16-.25.25-.42.08-.17.04-.32-.02-.44-.06-.13-.58-1.39-.8-1.9-.21-.5-.43-.44-.58-.45-.15-.01-.32-.01-.5-.01-.17 0-.44.06-.67.28-.23.22-.89.87-.89 2.13 0 1.26.91 2.48 1.04 2.65.13.17 1.79 2.74 4.32 3.73.61.21 1.08.33 1.45.42.61.15 1.17.13 1.6.08.49-.06 1.54-.63 1.76-1.24.22-.62.22-1.16.16-1.24-.06-.09-.23-.14-.5-.27z" /></svg>
  WhatsApp
</a>

<!-- CONTENIDO PRINCIPAL -->
<main class="w-screen h-screen overflow-x-hidden">

  <!-- SECCIÓN INICIO -->
  <section id="inicio" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
    <!-- Imagen de fondo -->
    <img
      src="/inicio-bg.png" 
      alt="Taekwondo fondo"
      class="absolute inset-0 w-full h-full object-cover z-0 select-none"
      draggable="false"
    />
    <div class="absolute inset-0 bg-black/70 z-10"></div>
    <!-- Contenido principal -->
    <div class="relative z-20 flex flex-col items-center text-center w-full max-w-xl">
      <img src="/ladcar-logo.jpg" alt="LADCAR" class="w-16 h-16 rounded-full border-2 border-yellow-400 shadow mb-2 mx-auto"/>
      <span class="text-3xl font-bold text-white">INSTITUTO LADCAR DE MÉXICO</span>
      <div class="h-1 w-24 bg-yellow-400 my-1 rounded-full mx-auto"></div>
      <span class="text-xl font-bold tracking-widest text-red-500 mb-2">TAEKWONDO</span>
      <p class="text-lg md:text-xl text-gray-200 mt-3 mb-8 font-medium drop-shadow-md">
        Disciplina, respeto y superación personal en cada clase.<br>
        Aprende defensa, mejora tu condición y forma parte de nuestra comunidad.
      </p>
      <div class="flex gap-4 justify-center">
        <button class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-8 rounded-full shadow transition"
          on:click={() => scrollToSection('ladcar')}>
          Más información
        </button>
        <button class="bg-yellow-400 hover:bg-yellow-300 text-black font-bold py-3 px-8 rounded-full shadow transition"
          on:click={() => scrollToSection('promocion')}>
          Promociones
        </button>
      </div>
    </div>
  </section>

  <!-- SECCIÓN POR QUÉ LADCAR -->
  <section id="ladcar" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
    <img
      src="/porque-bg.png"
      alt="Ambiente LADCAR"
      class="absolute inset-0 w-full h-full object-cover z-0 select-none"
      draggable="false"
    />
    <div class="absolute inset-0 bg-black/75 z-10"></div>
    <div class="relative z-20 flex flex-col items-center justify-center w-full h-full text-center">
      <h2 class="text-4xl font-bold text-yellow-400 mb-10">¿Por qué elegir LADCAR?</h2>
      <div class="flex flex-col md:flex-row gap-10 justify-center w-full max-w-4xl">
        <div class="flex flex-col items-center">
          <span class="text-6xl mb-4">🥋</span>
          <h3 class="text-2xl font-semibold text-white mb-2">Disciplina y respeto</h3>
          <p class="text-gray-200 text-lg max-w-xs">
            Formamos personas íntegras, promoviendo valores dentro y fuera del tatami.
          </p>
        </div>
        <div class="flex flex-col items-center">
          <span class="text-6xl mb-4">🎓</span>
          <h3 class="text-2xl font-semibold text-white mb-2">Instructores certificados</h3>
          <p class="text-gray-200 text-lg max-w-xs">
            Entrena con profesionales avalados y con amplia experiencia en TaeKwonDo.
          </p>
        </div>
        <div class="flex flex-col items-center">
          <span class="text-6xl mb-4">🤝</span>
          <h3 class="text-2xl font-semibold text-white mb-2">Ambiente familiar</h3>
          <p class="text-gray-200 text-lg max-w-xs">
            Un espacio seguro y amigable para niños, jóvenes y adultos.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- SECCIÓN PROMOCIÓN -->
  <section id="promocion" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
    <img
      src="/promocion-bg.png"
      alt="Promoción LADCAR"
      class="absolute inset-0 w-full h-full object-cover z-0 select-none"
      draggable="false"
    />
    <div class="absolute inset-0 bg-black/75 z-10"></div>
    <div class="relative z-20 flex flex-col items-center justify-center text-center w-full max-w-2xl">
      <h2 class="text-4xl font-bold text-yellow-400 mb-5">¡Aprovecha nuestra promoción especial!</h2>
      <p class="text-xl md:text-2xl text-white mb-2 font-semibold">
        Inscripción + Mensualidad + Uniforme oficial
      </p>
      <div class="bg-yellow-400 text-black font-bold rounded px-4 py-2 text-2xl mb-6">$1,200 MXN</div>
      <ul class="text-green-400 text-lg mb-6 space-y-1">
        <li>✔️ Inscripción</li>
        <li>✔️ Mensualidad</li>
        <li>✔️ Uniforme oficial</li>
      </ul>
      <a href={whatsappLink} target="_blank" rel="noopener"
        class="inline-flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-8 rounded-full shadow-lg text-lg transition-all">
        Solicita tu promoción
      </a>
    </div>
  </section>

  <!-- SECCIÓN UBICACIÓN -->
  <section id="ubicacion" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
    <img
      src="/ubicacion-bg.jpg"
      alt="Ubicación LADCAR"
      class="absolute inset-0 w-full h-full object-cover z-0 select-none"
      draggable="false"
    />
    <div class="absolute inset-0 bg-black/80 z-10"></div>
    <div class="relative z-20 flex flex-col items-center justify-center text-center w-full max-w-xl">
      <h2 class="text-4xl font-bold text-yellow-400 mb-6">¿Dónde estamos?</h2>
      <div class="text-lg text-white mb-3 font-semibold">Av. Ejemplo 123, Colonia Centro, Ciudad, Estado</div>
      <div class="text-gray-300 mb-6">¡Visítanos o escríbenos para más información!</div>
      <div class="w-full h-56 rounded-xl overflow-hidden shadow-lg border-2 border-yellow-400/40 mx-auto">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3732.391892872539!2d-110.9458786!3d27.9392732!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjfCsDU2JzIyLjQiTiAxMTDCsDU2JzQxLjAiVw!5e0!3m2!1ses-419!2smx!4v1718842000000"
          width="100%" height="100%" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"
          class="w-full h-full"></iframe>
      </div>
    </div>
  </section>

  <!-- SECCIÓN CONTACTO -->
  <section id="contacto" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
    <img
      src="/contacto-bg.png"
      alt="Contacto LADCAR"
      class="absolute inset-0 w-full h-full object-cover z-0 select-none"
      draggable="false"
    />
    <div class="absolute inset-0 bg-black/80 z-10"></div>
    <div class="relative z-20 flex flex-col items-center justify-center text-center w-full max-w-xl">
      <h2 class="text-4xl font-bold text-yellow-400 mb-5">¿Listo para comenzar?</h2>
      <p class="text-white text-xl mb-6">¡Escríbenos por WhatsApp y asegura tu lugar con uniforme incluido!</p>
      <a href={whatsappLink} target="_blank" rel="noopener"
        class="inline-flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-8 rounded-full shadow-lg text-lg transition-all">
        Solicita tu promoción
      </a>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="w-full bg-black/90 border-t border-[#232325] text-gray-400 text-center py-6">
    <div class="mb-1 font-bold text-yellow-400">Instituto LADCAR</div>
    <div class="mb-1">Av. Ejemplo 123, Colonia Centro, Ciudad, Estado</div>
    <div class="mb-1">WhatsApp: <a href={whatsappLink} class="underline hover:text-yellow-400 transition">+52 XXXXXXXX</a></div>
    <div>
      <span class="mr-2">Síguenos:</span>
      <a href="#" class="inline-block mx-1 hover:text-red-400 transition">Facebook</a>
      <a href="#" class="inline-block mx-1 hover:text-red-400 transition">Instagram</a>
    </div>
    <div class="mt-2 text-xs text-gray-500">&copy; {new Date().getFullYear()} Instituto LADCAR. Todos los derechos reservados.</div>
  </footer>
</main>

