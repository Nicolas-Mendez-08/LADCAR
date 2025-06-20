<script lang="ts">
  /**
   * Sección de Contacto.
   * Props:
   * - whatsappLink: link para botón de promoción.
   */
  export let whatsappLink: string;
</script>

<section id="contacto" class="relative w-screen h-screen flex items-center justify-center overflow-hidden">
  <img
    src="/contacto-bg.jpg"
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
