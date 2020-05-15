<template lang="pug">
  .container
    .navbar
      img.brand-logo(src="/logo.png")
      a.link(href="#contato") Entre em contato
    nuxt
</template>

<style lang="postcss" scoped>
.container {
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
