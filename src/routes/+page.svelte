<script lang="ts">
  import FloatingNav from '$lib/components/FloatingNav.svelte';
  import WhatsAppButton from '$lib/components/WhatsAppButton.svelte';
  import SectionInicio from '$lib/components/SectionInicio.svelte';
  import SectionPorqueLadcar from '$lib/components/SectionPorqueLadcar.svelte';
  import SectionPromocion from '$lib/components/SectionPromocion.svelte';
  import SectionUbicacion from '$lib/components/SectionUbicacion.svelte';
  import SectionContacto from '$lib/components/SectionContacto.svelte';
  import FooterLadcar from '$lib/components/FooterLadcar.svelte';

  // Configuración general
  const whatsappNumber = "52XXXXXXXXXX";
  const whatsappMessage = encodeURIComponent("Quiero mi promoción");
  const whatsappLink = `https://wa.me/${whatsappNumber}?text=${whatsappMessage}`;

  const nav = [
    { id: "inicio", icon: "🏠", label: "Inicio" },
    { id: "ladcar", icon: "⭐", label: "¿Por qué LADCAR?" },
    { id: "promocion", icon: "🎁", label: "Promoción" },
    { id: "ubicacion", icon: "📍", label: "Ubicación" },
    { id: "contacto", icon: "✅", label: "Contacto" },
  ];

  function scrollToSection(id: string) {
    const el = document.getElementById(id);
    if (el) el.scrollIntoView({ behavior: "smooth", block: "start" });
  }
</script>

<FloatingNav {nav} {scrollToSection} />
<WhatsAppButton {whatsappLink} />
<main>
  <SectionInicio
    onInfoClick={() => scrollToSection('ladcar')}
    onPromoClick={() => scrollToSection('promocion')}
  />
  <SectionPorqueLadcar />
  <SectionPromocion {whatsappLink} />
  <SectionUbicacion />
  <SectionContacto {whatsappLink} />
  <FooterLadcar {whatsappLink} year={new Date().getFullYear()} />
</main>
