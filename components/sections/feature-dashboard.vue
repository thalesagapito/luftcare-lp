<template lang="pug">
  section.wrapper
    .text-column
      feature-icon(color-mode="light" icon="medical")
      .title Painel de controle médico
      .description Médicos podem acompanhar o tratamento de todos os seus pacientes a distância. Com acesso aos testes de controle da asma, pico de fluxo e queixas dos pacientes, é possível enxergar a progressão no manejo da doença e intervir quando necessário.

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
