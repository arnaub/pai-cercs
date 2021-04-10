<template>
  <footer class="footer">
    <FooterClouds v-if="$colorMode.value === 'dark'" class="footer-image" />
    <FooterFlowers v-else class="footer-image" />
  </footer>
</template>

<script>
import FooterFlowers from '~/components/icons/flors-footer.svg?inline';
import FooterClouds from '~/components/icons/nuvols-footer.svg?inline';

export default {
  components: {
    FooterFlowers,
    FooterClouds
  }
}
</script>

<style lang="postcss" scoped>
.footer {
  width: 100%;
}

.footer-image {
}
</style>
