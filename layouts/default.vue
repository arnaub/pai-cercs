<template>
  <div class="container">
    <Header class="header"/>
    <nuxt />
    <Footer />
    <AnimatedGreyBackground v-if="$colorMode.value === 'dark'" class="background-forms"/>
    <AnimatedBackground v-else class="background-forms"/>
  </div>
</template>

<script>
import Header from '~/components/general/Header.vue'
import ColorModePicker from '~/components/general/ColorModePicker.vue'
import Footer from '~/components/general/Footer.vue'
import AnimatedBackground from '~/components/sections/AnimatedBackground.vue'
import AnimatedGreyBackground from '~/components/sections/AnimatedGreyBackground.vue'

export default {
  components: {
    Header,
    ColorModePicker,
    Footer,
    AnimatedBackground,
    AnimatedGreyBackground
  }
}
</script>

<style lang="postcss" scoped>
.container {
  position: relative;
  overflow: hidden;
}

.header {
  z-index: 1;
}

.background-forms {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: -1;
}
</style>
