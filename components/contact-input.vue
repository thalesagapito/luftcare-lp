<template lang="pug">
  .contact-input-wrapper
    input(
      type="email"
      autocomplete="email"
      aria-label="Seu endereço de email"
      placeholder="Seu endereço de email"
    )
    button(
      type="submit"
    ) Vamos conversar
</template>

<script>
export default {}
</script>

<style lang="postcss" scoped>
.contact-input-wrapper {
  @apply bg-white rounded shadow-xl flex flex-col p-3 font-light w-full;

  input,
  button {
    @apply h-16;
  }

  input {
    @apply text-center;
  }
  button {
    @apply bg-gray-800 text-gray-100 rounded;
  }
}

@screen md {
  .contact-input-wrapper {
    @apply flex-row p-4;

    input,
    button {
      @apply flex-1;
    }

    input {
      @apply text-left px-2;
    }
  }
}
</style>
