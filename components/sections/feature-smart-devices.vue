<template lang="pug">
  section
    .content-wrapper
      .text-column
        feature-icon(color-mode="dark" icon="idea")
        .title Dispositivos inteligentes
        .description Com a nossa bombinha de asma inteligente, é possível registrar o uso da medicação e testar a capacidade pulmonar do paciente (teste de pico de fluxo). Tudo isso registrado no aplicativo.
      .inhaler: img(src="/inhaler-blueprint.png" alt="Desenho em giz de uma bombinha de asma recebendo e enviando dados.")
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
.content-wrapper {
  @apply max-w-2xl mx-auto flex flex-col items-center;

  .text-column {
    @apply flex flex-col items-center text-center;

    .title {
      @apply text-xl font-semibold mt-5 mb-2;
    }
    .description {
      @apply text-lg font-light text-gray-200;
    }
  }

  .inhaler {
    @apply mx-auto h-64;
    img {
      @apply h-full mx-auto;
    }
  }
}

@screen md {
  .content-wrapper {
    @apply max-w-4xl flex-row-reverse;

    .text-column {
      @apply items-end text-right flex-1 mb-16;
    }

    .inhaler {
      @apply flex-1;
      height: 20rem;
    }
  }
}
@screen lg {
  .content-wrapper {
    @apply max-w-5xl;

    .inhaler {
      @apply flex-1;
      height: 22rem;
    }
  }
}
</style>
