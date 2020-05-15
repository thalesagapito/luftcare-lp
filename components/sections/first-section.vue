<template lang="pug">
  section.wrapper
    .title Entregamos saúde na palma da sua mão.
    .subtitle Através do monitoramento constante de sintomas da asma, damos aos médicos a capacidade de acompanhar seus pacientes e tomar decisões mais embasadas.
</template>

<script>
export default {}
</script>

<style lang="postcss" scoped>
.wrapper {
  @apply flex flex-col items-center mt-10 text-center font-light pb-14 mx-auto max-w-lg px-4;

  .title {
    @apply text-4xl text-white;
  }
  .subtitle {
    @apply text-lg text-gray-200 mt-5 leading-loose;
  }
}
@screen md {
  .wrapper {
    @apply max-w-2xl;
    .title {
      @apply text-5xl;
    }
    .subtitle {
      @apply text-xl;
    }
  }
}
</style>
