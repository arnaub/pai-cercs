<template>
  <Forest class="animated-forest" />
</template>

<script>
import Forest from '~/components/icons/bosc.svg?inline'

export default {
  components: {
    Forest
  },
  mounted() {
    console.log("forest mounted")
    this.animateIcon();
  },
  methods: {
    animateIcon() {
      const anime = this.$anime
      anime({
        targets: '.animated-forest .animate-cloud',
        opacity: [
          {value: 1, duration: 4000, delay: 0},
          {value: 0, duration: 8000, delay: 8000}
        ],
        translateX: -300,
        scaleX: 1.05,
        duration: 20000,
        easing: 'linear',
        loop: true,
        endDelay: 10000,
      })
    }
  },
}
</script>

<style lang="postcss" scoped>
.animate-cloud {
  opacity: 0;
}
</style>
