<template>
  <div class="container">
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/general/Header.vue'
import ColorModePicker from '~/components/general/ColorModePicker.vue'
import Footer from '~/components/general/Footer.vue'

export default {
  components: {
    Header,
    ColorModePicker,
    Footer,
  }
}
</script>
