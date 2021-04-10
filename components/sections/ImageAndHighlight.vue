<template>
  <section class="text-image-wrapper">
    <div class="section-image">
      <Rain v-if="$colorMode.value === 'dark'" />
      <Flowers v-else />
    </div>
    <div class="section-info">
      <h2 class="section-title">Ipsum dolor sit amet, consectetuer adipiscing elit, sed diam</h2>
    </div>
  </section>
</template>

<script>
import Flowers from '~/components/icons/flors.svg?inline'
import Rain from '~/components/icons/pluja.svg?inline'
export default {
  components: {
    Flowers,
    Rain
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
  margin: var(--big-gap) 0;
}
.section-image {
  grid-column-start: 2;
  grid-column-end: span 4;
  height: 20vw;
}

.section-image-image{
  width: 100%;
}

.section-description:last-child {
  margin-bottom: 0;
}

.section-info {
  grid-column-start: 8;
  grid-column-end: span 4;
  justify-self: center;
  align-self: center;
  text-align: center;
}
</style>
