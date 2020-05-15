<template lang="pug">
  .container
    first-section
    feature-app.feature
    feature-smart-devices.feature.dark
    feature-dashboard.feature
</template>

<script>
import FirstSection from '~/components/sections/first-section.vue'
import FeatureApp from '~/components/sections/feature-app.vue'
import FeatureSmartDevices from '~/components/sections/feature-smart-devices.vue'
import FeatureDashboard from '~/components/sections/feature-dashboard.vue'

export default {
  components: {
    FirstSection,
    FeatureApp,
    FeatureSmartDevices,
    FeatureDashboard
  }
}
</script>

<style lang="postcss" scoped>
.feature {
  @apply pt-10 flex flex-col items-center px-4 bg-white;
  &.dark {
    @apply bg-avocado text-white;
  }
}
</style>
