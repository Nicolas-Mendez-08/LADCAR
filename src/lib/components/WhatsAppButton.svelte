<script lang="ts">
  /**
   * Botón flotante de WhatsApp.
   * Props:
   * - whatsappLink: string con el link a WhatsApp
   * - label: texto a mostrar (opcional)
   * - className: clases extra para personalizar (opcional)
   */
  export let whatsappLink: string;
  export let label: string = "WhatsApp";
  export let className: string = "";
</script>

<a
  href={whatsappLink}
  target="_blank"
  rel="noopener"
  class={"fixed bottom-6 right-6 z-50 flex items-center gap-2 bg-green-500 hover:bg-green-600 text-white font-bold px-5 py-3 rounded-full shadow-xl text-lg transition-all ring-2 ring-white " + className}
>
  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
    stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
    d="M16.72 12.06c-.26-.13-1.54-.76-1.77-.85-.24-.08-.41-.13-.58.13-.17.25-.67.85-.83 1.02-.15.17-.31.19-.57.06-.26-.13-1.09-.4-2.08-1.29-.77-.69-1.29-1.54-1.44-1.8-.15-.26-.02-.4.11-.53.11-.11.25-.29.37-.44.12-.15.16-.25.25-.42.08-.17.04-.32-.02-.44-.06-.13-.58-1.39-.8-1.9-.21-.5-.43-.44-.58-.45-.15-.01-.32-.01-.5-.01-.17 0-.44.06-.67.28-.23.22-.89.87-.89 2.13 0 1.26.91 2.48 1.04 2.65.13.17 1.79 2.74 4.32 3.73.61.21 1.08.33 1.45.42.61.15 1.17.13 1.6.08.49-.06 1.54-.63 1.76-1.24.22-.62.22-1.16.16-1.24-.06-.09-.23-.14-.5-.27z" /></svg>
  {label}
</a>
