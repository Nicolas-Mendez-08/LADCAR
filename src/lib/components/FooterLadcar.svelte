<script lang="ts">
  /**
   * Footer de la página.
   * Props:
   * - whatsappLink: string para contacto rápido
   * - year: año actual, por default usa el año en curso
   */
  export let whatsappLink: string;
  export let year: number = new Date().getFullYear();
</script>

<footer class="w-full bg-black/90 border-t border-[#232325] text-gray-400 px-8 py-7">
  <div class="max-w-6xl mx-auto flex flex-col md:flex-row md:items-center md:justify-between gap-6 md:gap-0">
    <div class="flex flex-row items-center gap-4 justify-center md:justify-start">
      <img
        src="/ladcar-logo.jpg"
        alt="LADCAR logo"
        class="w-14 h-14 rounded-xl shadow-lg border-2 border-yellow-400 bg-white object-contain"
      />
      <div>
        <div class="font-extrabold text-yellow-400 text-lg leading-tight">Instituto LADCAR</div>
        <div class="text-sm text-gray-300">Taekwondo Profesional</div>
      </div>
    </div>
    <div class="text-center md:text-left flex flex-col gap-1">
      <div class="text-sm text-gray-300">
        Av. Ejemplo 123, Colonia Centro, Ciudad, Estado
      </div>
      <div class="text-sm">
        WhatsApp: 
        <a href={whatsappLink} class="ml-2 underline hover:text-yellow-400 transition font-bold">
          +52 XXXXXXXX
        </a>
      </div>
    </div>
    <div class="flex flex-col items-center md:items-end gap-2">
      <span class="text-sm text-gray-300">Síguenos:</span>
      <div class="flex flex-row gap-3">
        <a href="#" aria-label="Facebook" class="hover:text-blue-400 transition text-2xl">
          <svg fill="currentColor" class="w-7 h-7" viewBox="0 0 24 24"><path d="M22.676 0h-21.352c-.732 0-1.324.592-1.324 1.324v21.352c0 .732.592 1.324 1.324 1.324h11.495v-9.294h-3.129v-3.622h3.129v-2.672c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.462.099 2.796.143v3.24l-1.918.001c-1.504 0-1.797.715-1.797 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116c.732 0 1.324-.592 1.324-1.324v-21.352c0-.732-.592-1.324-1.324-1.324z"/></svg>
        </a>
        <a href="#" aria-label="Instagram" class="hover:text-pink-400 transition text-2xl">
          <svg fill="currentColor" class="w-7 h-7" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 1.366.062 2.633.342 3.608 1.317.975.975 1.255 2.242 1.317 3.608.058 1.266.069 1.646.069 4.85s-.012 3.584-.07 4.85c-.062 1.366-.342 2.633-1.317 3.608-.975.975-2.242 1.255-3.608 1.317-1.266.058-1.646.069-4.85.069s-3.584-.012-4.85-.07c-1.366-.062-2.633-.342-3.608-1.317-.975-.975-1.255-2.242-1.317-3.608C2.175 15.647 2.163 15.267 2.163 12s.012-3.584.07-4.85c.062-1.366.342-2.633 1.317-3.608.975-.975 2.242-1.255 3.608-1.317C8.416 2.175 8.796 2.163 12 2.163zm0-2.163C8.741 0 8.332.012 7.053.07 5.775.128 4.602.387 3.678 1.312c-.924.924-1.184 2.097-1.242 3.375C2.012 5.741 2 6.15 2 12s.012 6.259.07 7.548c.058 1.278.318 2.451 1.242 3.375.924.924 2.097 1.184 3.375 1.242C8.332 23.988 8.741 24 12 24s3.668-.012 4.947-.07c1.278-.058 2.451-.318 3.375-1.242.924-.924 1.184-2.097 1.242-3.375C21.988 18.259 22 17.85 22 12s-.012-6.259-.07-7.548c-.058-1.278-.318-2.451-1.242-3.375-.924-.924-2.097-1.184-3.375-1.242C15.668.012 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 0 0 0-12.324zm0 10.162a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.88 1.44 1.44 0 0 0 0-2.88z"/></svg>
        </a>
        <a href="#" aria-label="WhatsApp" class="hover:text-green-400 transition text-2xl">
          <svg fill="currentColor" class="w-7 h-7" viewBox="0 0 24 24"><path d="M12.004 2.003A9.936 9.936 0 0 0 2 12.003c0 1.762.459 3.435 1.264 4.89L2 22l5.212-1.245A9.955 9.955 0 0 0 12.004 22a9.937 9.937 0 0 0 9.996-9.997c0-5.522-4.478-10-9.996-10zm0 18.28a8.314 8.314 0 0 1-4.267-1.217l-.307-.184-3.097.741.66-3.028-.199-.312A8.313 8.313 0 0 1 3.678 12c0-4.593 3.73-8.32 8.326-8.32 4.591 0 8.322 3.727 8.322 8.32 0 4.591-3.731 8.318-8.322 8.318zm4.51-6.339c-.248-.124-1.469-.729-1.696-.812-.227-.083-.392-.124-.557.125-.164.248-.634.812-.777.979-.143.166-.286.187-.534.063-.249-.125-1.05-.387-2-1.234-.74-.657-1.236-1.467-1.382-1.715-.144-.248-.016-.382.108-.505.112-.113.249-.293.373-.439.125-.147.166-.248.248-.414.082-.166.041-.312-.02-.438-.062-.125-.557-1.343-.762-1.841-.201-.48-.406-.416-.557-.424l-.475-.008c-.166 0-.437.062-.666.311-.229.25-.875.855-.875 2.084 0 1.229.896 2.417 1.021 2.584.124.166 1.762 2.687 4.306 3.672.602.207 1.07.33 1.436.422.604.154 1.153.133 1.589.081.485-.057 1.469-.601 1.678-1.182.209-.581.209-1.079.146-1.182-.062-.104-.227-.166-.476-.291z"/></svg>
        </a>
      </div>
    </div>
  </div>
  <div class="text-center text-xs text-gray-500 mt-7 mb-2">&copy; {year} Instituto LADCAR. Todos los derechos reservados.</div>
</footer>
