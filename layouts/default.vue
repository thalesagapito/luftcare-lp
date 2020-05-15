<template lang="pug">
  .page-wrapper
    .navbar.container
      img.brand-logo(src="/logo.png")
      a.link(href="#contato") Entre em contato
    nuxt
</template>

<style lang="postcss" scoped>
.page-wrapper {
  @apply flex flex-col items-center justify-start mx-auto;

  .navbar {
    @apply flex justify-between w-full px-4 py-8;
    .brand-logo {
      @apply h-6;
    }
    .link {
      @apply text-white;
    }
  }
}
</style>
