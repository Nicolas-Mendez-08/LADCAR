<script lang="ts">
  export let onInfoClick: () => void;
  export let onPromoClick: () => void;
</script>

<section
  id="inicio"
  class="relative w-screen h-screen flex items-start justify-start overflow-hidden font-sans"
  style="min-height: 600px;"
>
  <!-- Fondo elegante -->
  <div class="absolute inset-0 z-0">
    <div
      class="absolute inset-0"
      style="
        background: radial-gradient(ellipse at 80% 70%, rgba(255,255,255,0.13) 0%, rgba(255,230,100,0.10) 36%, rgba(25,20,5,0.89) 100%);
      "
    ></div>
    <div
      class="absolute inset-0"
      style="
        background: linear-gradient(135deg, #29231a 0%, #e3b43e 55%, #fff3b0 100%);
        opacity: 0.80;
      "
    ></div>
  </div>

  <!-- Header superior izquierdo -->
  <div class="absolute top-8 left-[10vw] flex items-center z-20">
    <img
      src="/ladcar-logo.jpg"
      alt="Escudo LADCAR"
      class="w-16 h-16 md:w-20 md:h-20 rounded-lg shadow-xl border-4 border-yellow-400 bg-white object-contain"
    />
    <div class="ml-4 flex flex-col">
      <span class="text-2xl md:text-3xl font-extrabold text-black drop-shadow leading-tight">
        Instituto Ladcar de México
      </span>
      <span class="w-36 h-1 bg-yellow-400 my-1 rounded-full"></span>
      <span class="text-lg md:text-xl font-bold tracking-widest" style="letter-spacing: 0.15em;">
        <span
          class="inline-block animate-pulse bg-gradient-to-r from-yellow-400 via-yellow-100 to-yellow-400 bg-clip-text text-transparent"
          style="animation: taekwondoGlow 2s infinite alternate;"
        >
          Taekwondo
        </span>
      </span>
    </div>
  </div>

  <!-- HERO: texto y foto con 10% de separación a cada lado -->
  <div
    class="relative z-20 flex flex-row items-center w-full h-full"
    style="padding-left:10vw; padding-right:10vw;"
  >
    <!-- Texto principal (crece hasta la imagen, solo 10px de separación) -->
    <div
      class="flex flex-col justify-center flex-1 min-w-0"
      style="margin-right:10px;"
    >
      <h1 class="text-2xl md:text-4xl font-black text-black drop-shadow mb-2 uppercase tracking-tight leading-tight">
        ¿QUIERES MEJORAR EL<br />
        COMPORTAMIENTO DE TU HIJO<br />
        EN UN <span class="text-yellow-400">60%</span>?
      </h1>
      <p class="text-lg md:text-xl font-semibold text-black mb-6 mt-2">
        Mejoramos disciplina, enfoque y respeto.
      </p>
      <div class="flex gap-4 mt-1">
        <button
          class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-8 rounded-full shadow-lg transition-all text-base"
          on:click={onInfoClick}
        >
          Más información
        </button>
        <button
          class="bg-yellow-400 hover:bg-yellow-300 text-black font-bold py-3 px-8 rounded-full shadow-lg transition-all text-base"
          on:click={onPromoClick}
        >
          Promociones
        </button>
      </div>
    </div>
    <!-- IMAGEN: GRANDE Y OCULTA EN ≤900px -->
    <div class="flex-shrink-0 flex items-end h-full">
      <img
        src="/instructor-y-alumno.png"
        alt="Instructor y alumno"
        class="hero-image pointer-events-none select-none"
        style="object-fit: contain; max-height: 75vh; width: auto;"
        draggable="false"
      />
    </div>
  </div>

  <!-- Animación personalizada para "Taekwondo" -->
  <style>
    @keyframes taekwondoGlow {
      0% { filter: brightness(1) drop-shadow(0 0 3px #ffe066); }
      50% { filter: brightness(1.3) drop-shadow(0 0 10px #ffe066); }
      100% { filter: brightness(1) drop-shadow(0 0 3px #ffe066); }
    }
    @media (max-width: 900px) {
      .hero-image {
        display: none !important;
      }
    }
  </style>
</section>
