<template lang="pug">
  section
    .content-wrapper
      .text-column
        feature-icon(color-mode="light" icon="medical")
        .title Painel de controle médico
        .description Médicos podem acompanhar o tratamento de todos os seus pacientes a distância. Com acesso aos testes de controle da asma, pico de fluxo e queixas dos pacientes, é possível enxergar a progressão no manejo da doença e intervir quando necessário.
      .devices-container
        macbook
        iphone
</template>

<script>
import Macbook from '~/components/device-frames/macbook.vue'
import Iphone from '~/components/device-frames/iphone.vue'
import FeatureIcon from '~/components/feature-icon.vue'

export default {
  components: {
    FeatureIcon,
    Macbook,
    Iphone
  }
}
</script>

<style lang="postcss" scoped>
.content-wrapper {
  @apply pb-5 mx-auto;
  .text-column {
    @apply flex flex-col items-center text-center;
    .title {
      @apply text-xl font-semibold mt-5 mb-2;
    }
    .description {
      @apply text-lg font-light text-gray-600;
    }
  }
  .devices-container {
    @apply relative w-full;
    height: 20rem;
    & >>> .macbook,
    & >>> .iphone-x {
      @apply absolute origin-bottom-left bottom-0;
      left: 50%;
    }
    & >>> .macbook {
      transform: scale(0.4) translate(-20%, -2%);
    }
    & >>> .iphone-x {
      transform: scale(0.3) translate(-100%, 0);
    }
  }
}

@screen md {
  .content-wrapper {
    @apply max-w-4xl;
    .devices-container {
      height: 26rem;

      & >>> .macbook {
        transform: scale(0.5) translate(-50%, -5%);
      }
      & >>> .iphone-x {
        transform: scale(0.37) translate(110%, 0);
      }
    }
  }
}
@screen lg {
  .content-wrapper {
    @apply max-w-5xl;
    .devices-container {
      height: 35rem;

      & >>> .macbook {
        transform: scale(0.7) translate(-50%, -5%);
      }
      & >>> .iphone-x {
        transform: scale(0.5) translate(110%, 0);
      }
    }
  }
}
</style>
