<script lang="ts">
  /**
   * Menú flotante de navegación a secciones.
   * Props:
   * - nav: Array con { id, icon, label }
   * - scrollToSection: función para hacer scroll a la sección
   */
  export let nav = [];
  export let scrollToSection: (id: string) => void;
</script>

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
