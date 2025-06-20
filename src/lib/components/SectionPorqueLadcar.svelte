<script lang="ts">
  // Sección ¿Por qué elegir LADCAR?
</script>

<section
  id="ladcar"
  class="relative w-screen h-screen flex items-center justify-center overflow-hidden"
>
  <!-- Fondo con imagen y degradado elegante -->
  <img
    src="/porque-bg.png"
    alt="Ambiente LADCAR"
    class="absolute inset-0 w-full h-full object-cover z-0 select-none"
    draggable="false"
  />
  <!-- Overlay: degradado negro a transparente para más profundidad -->
  <div class="absolute inset-0 z-10 bg-gradient-to-br from-black/70 via-black/50 to-transparent"></div>
  
  <div class="relative z-20 flex flex-col items-center justify-center w-full h-full text-center px-4 md:px-0">
    <h2 class="text-3xl md:text-4xl font-extrabold text-yellow-400 mb-2 tracking-tight">
      ¿Por qué elegir LADCAR?
    </h2>
    <div class="w-20 h-1 bg-yellow-400 mb-10 rounded-full"></div>
    
    <div class="flex flex-col md:flex-row gap-8 md:gap-12 justify-center w-full max-w-5xl">
      <!-- Card 1 -->
      <div class="bg-white/10 backdrop-blur-lg rounded-2xl shadow-2xl border border-white/15 flex flex-col items-center p-7 md:p-8 transition hover:scale-[1.04] hover:bg-white/20 duration-200 max-w-xs mx-auto">
        <span class="text-6xl mb-3 drop-shadow">🥋</span>
        <h3 class="text-xl md:text-2xl font-bold text-yellow-300 mb-2">Disciplina y respeto</h3>
        <p class="text-gray-100 text-base md:text-lg">
          Formamos personas íntegras, promoviendo valores dentro y fuera del tatami.
        </p>
      </div>
      <!-- Card 2 -->
      <div class="bg-white/10 backdrop-blur-lg rounded-2xl shadow-2xl border border-white/15 flex flex-col items-center p-7 md:p-8 transition hover:scale-[1.04] hover:bg-white/20 duration-200 max-w-xs mx-auto">
        <span class="text-6xl mb-3 drop-shadow">🎓</span>
        <h3 class="text-xl md:text-2xl font-bold text-yellow-300 mb-2">Instructores certificados</h3>
        <p class="text-gray-100 text-base md:text-lg">
          Entrena con profesionales avalados y con amplia experiencia en TaeKwonDo.
        </p>
      </div>
      <!-- Card 3 -->
      <div class="bg-white/10 backdrop-blur-lg rounded-2xl shadow-2xl border border-white/15 flex flex-col items-center p-7 md:p-8 transition hover:scale-[1.04] hover:bg-white/20 duration-200 max-w-xs mx-auto">
        <span class="text-6xl mb-3 drop-shadow">🤝</span>
        <h3 class="text-xl md:text-2xl font-bold text-yellow-300 mb-2">Ambiente familiar</h3>
        <p class="text-gray-100 text-base md:text-lg">
          Un espacio seguro y amigable para niños, jóvenes y adultos.
        </p>
      </div>
    </div>
  </div>
</section>

<style>
  /* Responsive para altura mínima en mobile */
  @media (max-width: 700px) {
    section#ladcar { min-height: 850px !important; }
  }
</style>
