<template lang="pug">
  section.wrapper
    .text-column
      feature-icon(color-mode="light" icon="app")
      .title Teste de Controle da Asma (ACT)
      .description Temos um app fácil de usar que funciona em todas as plataformas. Pacientes podem realizar testes de controle da asma a qualquer momento em qualquer lugar.
    //- iphone

</template>

<script>
import Iphone from '~/components/device-frames/iphone.vue'
import FeatureIcon from '~/components/feature-icon.vue'

export default {
  components: {
    FeatureIcon,
    Iphone
  }
}
</script>

<style lang="postcss" scoped>
.wrapper {
  .text-column {
    @apply flex flex-col items-center text-center;

    .title {
      @apply text-xl font-semibold mt-5 mb-2;
    }
    .description {
      @apply text-lg font-light text-gray-600;
    }
  }
}
</style>
