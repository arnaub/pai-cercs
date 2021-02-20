<template>
  <section class="text-image-wrapper">
    <div class="section-image">
      <NuclearPlant />
    </div>
    <div class="section-info">
      <h2 class="section-title">Ipsum dolor sit amet, consectetuer adipiscing elit, sed diam</h2>
    </div>
  </section>
</template>

<script>
import NuclearPlant from '~/components/icons/central.svg?inline'
export default {
  components: {
    NuclearPlant
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
