<template>
  <section>
    <div class="section-header">
      <Helix v-if="$colorMode.value === 'dark'" class="section-header-image"/>
      <Leaf v-else class="section-header-image"/>
    </div>
    <div class="section-wrapper">
      <div class="section-box" :class="colorClass(index)" v-for="(box, index) in boxes" :key="index">
        <h3 class="box-title">{{box.title}}</h3>
        <p class="box-description">{{box.text}}</p>
      </div>
    </div>
  </section>
</template>

<script>

import Leaf from '~/components/icons/fulla.svg?inline'
import Helix from '~/components/icons/helix.svg?inline'

export default {
  props: ["title", "description", "boxes"],
  components: {
    Leaf,
    Helix
  },
  methods: {
    colorClass(index) {
      const classes = ["primary", "secondary", "tertiary", "quaternary"];
      return classes[index % classes.length];
    }
  }
}
</script>

<style lang="postcss" scoped>
section {
  margin: var(--big-gap) 0;
  margin-bottom: var(--big-gap);
}

.section-header {
  height: var(--gap);
  display: block;
}
.section-header-image{
  height: var(--gap);
  margin: 0 auto;
  display: block;
}

.section-wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--gap);
}

.section-title {
  font-size: var(--extra-big-text-size);
  margin-bottom: var(--gap);
}

.section-description {
  font-size: var(--big-text-size);
}

.box-title {
  margin: var(--small-gap) 0;
  font-size: var(--big-text-size);
}
.box-description {
  font-size: var(--text-size);
  line-height: var(--big-text-size);
  text-align: justify;
}


</style>
