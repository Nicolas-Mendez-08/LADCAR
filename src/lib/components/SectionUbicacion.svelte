<script lang="ts">
  /**
   * Sección de Ubicación.
   * Sin props, contenido estático.
   */
</script>

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
