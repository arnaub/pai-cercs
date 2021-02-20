<template>
  <section class="text-image-wrapper">
    <div class="section-info">
      <h2 class="section-title">Lorem ipsum dolor sit amet</h2>
      <p class="section-description">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus tempor, tortor eget ultricies lobortis, quam mi fermentum diam, feugiat dapibus erat ante et nulla. Quisque eu lacinia ligula. Proin tincidunt congue mauris, sit amet eleifend nisl egestas sit amet. Praesent rutrum quam in augue porttitor, malesuada aliquet enim lacinia.</p>
    </div>
    <div class="section-image">
      <NuclearPlant/>
    </div>
  </section>
</template>

<script>
import NuclearPlant from '~/components/icons/central.svg?inline'
export default {
  components: {
    NuclearPlant
  },
  mounted() {
    this.animateIcon()
  },
  methods: {
    animateIcon() {
      const anime = this.$anime
      anime({
        targets: '.st26',
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
        targets: '.st113',
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
.section-title {
  font-size: var(--extra-big-text-size);
  margin-bottom: var(--small-gap);
  font-weight: 300;
}
.text-image-wrapper {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  margin: var(--gap) 0;
}
.section-info {
  grid-column-start: 0;
  grid-column-end: span 6;
}

.section-description {
  line-height: 1.5em;
  text-align: justify;
}

.section-image {
  grid-column-start: 8;
  grid-column-end: span 5;
}

.st26, .st113 {
  opacity: 0;
}
</style>
