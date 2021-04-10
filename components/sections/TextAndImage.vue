<template>
  <section class="text-image-wrapper">
    <div class="section-info">
      <h2 class="section-title">Lorem ipsum dolor sit amet</h2>
      <p class="section-description">Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut lao- reet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam.</p>
      <p class="section-description">Quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat.</p>
      <p class="section-description">Vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.</p>
    </div>
    <div class="section-image">

      <AnimatedNuclear v-if="$colorMode.value === 'dark'" />
      <AnimatedForest v-else/>
    </div>
  </section>
</template>

<script>
import AnimatedForest from '~/components/sections/AnimatedForest'
import AnimatedNuclear from '~/components/sections/AnimatedNuclear'

export default {
  components: {
    AnimatedForest,
    AnimatedNuclear
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
.section-info {
  grid-column-start: 0;
  grid-column-end: span 6;
}

.section-description {
  line-height: 1.5em;
  font-size: var(--text-size);
  margin-bottom: var(--small-gap);
}

.section-description:last-child {
  margin-bottom: 0;
}

.section-image {
  grid-column-start: 7;
  grid-column-end: span 6;
}
</style>
