<script lang="ts">
  /**
   * Sección Promoción especial.
   * Props:
   * - whatsappLink: link para botón de promoción.
   */
  export let whatsappLink: string;
</script>

<section id="promocion" class="relative w-screen h-screen flex items-center justify-center overflow-hidden font-sans">
  <!-- Fondo con acción y overlay oscuro -->
  <img
    src="/promocion-bg.png"
    alt="Promoción LADCAR"
    class="absolute inset-0 w-full h-full object-cover z-0 select-none"
    draggable="false"
  />
  <div class="absolute inset-0 z-10 bg-gradient-to-br from-black/80 via-black/65 to-yellow-800/40"></div>
  
  <div class="relative z-20 flex flex-col md:flex-row items-center justify-center w-full h-full px-4 md:px-0 max-w-6xl mx-auto gap-10">
    <!-- Lado Izquierdo: Texto e información -->
    <div class="flex flex-col items-start justify-center w-full md:w-[420px] text-left">
      <h2 class="text-3xl md:text-4xl font-extrabold text-yellow-400 mb-3 tracking-tight uppercase drop-shadow">
        Descubre tu promoción
      </h2>
      <span class="block text-base md:text-lg text-white font-bold mb-3 italic">«El campeón de la vida llevas dentro»</span>
      <div class="w-28 h-1 bg-yellow-400 mb-5 rounded-full"></div>
      <!-- Paquete 1 -->
      <div class="bg-yellow-400 text-black font-extrabold rounded-lg px-6 py-3 text-xl mb-4 shadow-lg flex items-center gap-3">
        <span class="block font-bold text-2xl">Paquete 1</span>
        <span class="ml-auto text-2xl bg-black/80 px-3 py-1 rounded text-yellow-300 shadow-inner tracking-wider"> $900 </span>
      </div>
      <div class="pl-1 mb-2">
        <span class="bg-black/60 text-yellow-200 font-semibold px-2 py-1 rounded text-base shadow-sm">Mensualidad, uniforme e inscripción</span>
      </div>
      <!-- Paquete hermanos -->
      <div class="bg-yellow-500 text-black font-extrabold rounded-lg px-6 py-3 text-xl mb-4 shadow-lg flex items-center gap-3">
        <span class="block font-bold text-2xl">Paquete Hermanos</span>
        <span class="ml-auto text-2xl bg-black/80 px-3 py-1 rounded text-yellow-300 shadow-inner tracking-wider"> $1,600 </span>
      </div>
      <div class="pl-1 mb-6">
        <span class="bg-black/60 text-yellow-200 font-semibold px-2 py-1 rounded text-base shadow-sm">Mensualidad, uniforme e inscripción (2 alumnos)</span>
      </div>
      <!-- Botón WhatsApp -->
      <a href={whatsappLink} target="_blank" rel="noopener"
        class="mt-1 inline-flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-7 rounded-full shadow-lg text-lg transition-all focus:ring-4 focus:ring-green-400/30 ring-2 ring-white"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
          stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
          d="M16.72 12.06c-.26-.13-1.54-.76-1.77-.85-.24-.08-.41-.13-.58.13-.17.25-.67.85-.83 1.02-.15.17-.31.19-.57.06-.26-.13-1.09-.4-2.08-1.29-.77-.69-1.29-1.54-1.44-1.8-.15-.26-.02-.4.11-.53.11-.11.25-.29.37-.44.12-.15.16-.25.25-.42.08-.17.04-.32-.02-.44-.06-.13-.58-1.39-.8-1.9-.21-.5-.43-.44-.58-.45-.15-.01-.32-.01-.5-.01-.17 0-.44.06-.67.28-.23.22-.89.87-.89 2.13 0 1.26.91 2.48 1.04 2.65.13.17 1.79 2.74 4.32 3.73.61.21 1.08.33 1.45.42.61.15 1.17.13 1.6.08.49-.06 1.54-.63 1.76-1.24.22-.62.22-1.16.16-1.24-.06-.09-.23-.14-.5-.27z" /></svg>
        Solicita tu promoción
      </a>
      <!-- Teléfono -->
      <div class="mt-5 flex flex-col gap-1">
        <span class="text-base text-white/80 font-semibold tracking-wider">WhatsApp:</span>
        <span class="text-lg text-yellow-300 font-extrabold tracking-widest drop-shadow">622-138-74-16</span>
      </div>
    </div>
    <!-- Lado derecho: Imagen principal -->
    <div class="hidden md:flex flex-1 items-center justify-end h-full">
      <img
        src="/contacto-bg.jpg"
        alt="Combate Taekwondo LADCAR"
        class="max-h-[500px] w-auto rounded-2xl shadow-2xl object-cover border-4 border-yellow-400/70 bg-black/10"
        draggable="false"
      />
    </div>
  </div>
</section>

