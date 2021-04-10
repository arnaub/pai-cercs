<template>
  <NuclearPlant class="animated-nuclear"/>
</template>

<script>
import NuclearPlant from '~/components/icons/central.svg?inline'

export default {
  components: {
    NuclearPlant
  },
  mounted() {
    console.log("mounted nuclear")
    this.animateIcon();
  },
  methods: {
    animateIcon() {
      const anime = this.$anime
      anime({
        targets: '.animated-nuclear .animate-cloud',
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
      anime({
        targets: '.animated-nuclear .animate-fog',
        opacity: [
          {value: 1, duration: 2000, delay: 0},
        ],
        translateX: -1000,
        scaleX: 1.05,
        duration: 400000,
        easing: 'linear',
        loop: true,
        endDelay: 4000,
      })
    }
  },
}
</script>

<style lang="postcss" scoped>
.animate-cloud, .animate-fog {
  opacity: 0;
}
</style>
