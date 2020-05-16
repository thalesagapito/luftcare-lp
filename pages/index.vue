<template lang="pug">
  main.w-full
    title-section
    feature-app.feature
    feature-smart-devices.feature.dark
    feature-dashboard.feature
    contact-section#contato
</template>

<script>
import TitleSection from '~/components/sections/title-section.vue'
import ContactSection from '~/components/sections/contact-section.vue'
import FeatureApp from '~/components/sections/feature-app.vue'
import FeatureSmartDevices from '~/components/sections/feature-smart-devices.vue'
import FeatureDashboard from '~/components/sections/feature-dashboard.vue'

export default {
  components: {
    TitleSection,
    ContactSection,
    FeatureApp,
    FeatureSmartDevices,
    FeatureDashboard
  }
}
</script>

<style lang="postcss" scoped>
.feature {
  @apply pt-10 px-4 bg-white overflow-hidden;
  &.dark {
    @apply bg-avocado text-white;
  }
}
</style>
