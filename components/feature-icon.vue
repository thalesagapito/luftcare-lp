<template lang="pug">
  .wrapper-circle(:class="colorMode")
    i.md-icon {{ mdIconName }}

</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true,
      default: 'idea',
      validator: (v) => ['idea', 'app', 'medical'].includes(v)
    },
    colorMode: {
      type: String,
      required: true,
      default: 'light',
      validator: (v) => ['dark', 'light'].includes(v)
    }
  },
  computed: {
    mdIconName() {
      switch (this.icon) {
        case 'idea':
          return 'emoji_objects'
        case 'app':
          return 'phone_iphone'
        default:
          return 'local_hospital'
      }
    }
  }
}
</script>

<style lang="postcss" scoped>
.wrapper-circle {
  @apply w-14 h-14 rounded-full flex justify-center items-center text-3xl;
  &.light {
    @apply bg-avocado bg-opacity-20 text-avocado;
  }
  &.dark {
    @apply bg-teal-900 bg-opacity-60 text-white;
  }
}
</style>
