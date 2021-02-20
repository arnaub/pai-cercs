<template>
  <section>
    <div class="section-box" :class="colorClass(index)" v-for="(box, index) in boxes" :key="index">
      <h3 class="box-title">{{box.title}}</h3>
      <p class="box-description">{{box.text}}</p>
    </div>
  </section>
</template>

<script>

export default {
  props: ["title", "description", "boxes"],
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
