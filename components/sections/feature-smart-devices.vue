<template lang="pug">
  section.wrapper
    .text-column
      feature-icon(color-mode="dark" icon="idea")
      .title Dispositivos inteligentes
      .description Com a nossa bombinha de asma inteligente, é possível registrar o uso da medicação e testar a capacidade pulmonar do paciente (teste de pico de fluxo). Tudo isso registrado no aplicativo.
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
  @apply z-10;

  .text-column {
    @apply flex flex-col items-center text-center;

    .title {
      @apply text-xl font-semibold mt-5 mb-2;
    }
    .description {
      @apply text-lg font-light text-gray-200;
    }
  }
}
</style>
