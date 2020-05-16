<template lang="pug">
  section.wrapper
    .title Quer trazer a luftcare para o seu tratamento?
    .subtitle Se você é médico ou paciente e teve interesse na nossa solução, vamos conversar mais!
    contact-input.mt-5
</template>

<script>
import ContactInput from '~/components/contact-input.vue'
export default {
  components: {
    ContactInput
  }
}
</script>

<style lang="postcss" scoped>
.wrapper {
  @apply flex flex-col items-center my-16 text-center font-light pb-4 mx-auto max-w-lg px-4;

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
