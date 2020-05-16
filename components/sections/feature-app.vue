<template lang="pug">
  section
    .content-wrapper
      .text-column
        feature-icon(color-mode="light" icon="app")
        .title Teste de Controle da Asma (ACT)
        .description Temos um app fácil de usar que funciona em todas as plataformas. Pacientes podem realizar testes de controle da asma a qualquer momento em qualquer lugar.
      .devices-container
        nexus
        iphone

</template>

<script>
import Nexus from '~/components/device-frames/nexus.vue'
import Iphone from '~/components/device-frames/iphone.vue'
import FeatureIcon from '~/components/feature-icon.vue'

export default {
  components: {
    FeatureIcon,
    Iphone,
    Nexus
  }
}
</script>

<style lang="postcss" scoped>
.content-wrapper {
  @apply max-w-2xl mx-auto flex flex-col items-center;

  .text-column {
    @apply flex flex-col items-center text-center mb-5;

    .title {
      @apply text-xl font-semibold mt-5 mb-2;
    }
    .description {
      @apply text-lg font-light text-gray-600;
    }
  }

  .devices-container {
    @apply relative h-64 w-full overflow-hidden;

    & >>> .nexus5,
    & >>> .iphone-x {
      @apply absolute origin-top-left top-0;
      left: 50%;
    }
    & >>> .nexus5 {
      transform: scale(0.48) translateX(-100%);
    }
    & >>> .iphone-x {
      transform: scale(0.5) translate(-20%, 10%);
    }
  }
}

@screen md {
  .content-wrapper {
    @apply max-w-4xl flex-row;

    .text-column {
      @apply items-start text-left flex-1;
    }

    .devices-container {
      @apply flex-1 my-0;
      height: 20rem;

      & >>> .nexus5,
      & >>> .iphone-x {
        @apply left-0;
      }
      & >>> .nexus5 {
        transform: scale(0.45) translate(80%, 0%) rotate(15deg);
      }
      & >>> .iphone-x {
        transform: scale(0.4) translate(125%, 15%) rotate(15deg);
      }
    }
  }
}
@screen lg {
  .content-wrapper {
    @apply max-w-5xl;

    .devices-container {
      height: 32rem;

      & >>> .nexus5 {
        left: 0;
        transform: scale(0.57) translate(50%, 0%) rotate(15deg);
      }
      & >>> .iphone-x {
        left: 100%;
        transform: scale(0.49) translate(-100%, 20%) rotate(15deg);
      }
    }
  }
}
</style>
