<template>
  <section>
    <div class="section-info">
      <h2 class="section-title">{{title}}</h2>
      <p class="section-description">{{description}}</p>
    </div>
    <div class="section-box" :class="colorClass(index)" v-for="(box, index) in boxes" :key="index">
      <h5>{{box.title}}</h5>
      <p>{{box.text}}</p>
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
  gap: var(--small-gap);
}

.section-info {
  grid-column-start: 1;
  grid-column-end: span 2;
}

.section-title {
  font-size: var(--extra-big-text-size);
  margin-bottom: var(--gap);
}

.section-description {
  font-size: var(--big-text-size);
}

.section-box {
  border-radius: 5px;
  padding: var(--small-gap);
  background: var(--primary-color);
  height: 12rem;
}
.section-box.primary{
  background: var(--primary-color);
}

.section-box.secondary{
  background: var(--secondary-color);
}

.section-box.tertiary{
  background: var(--tertiary-color);
}

.section-box.quaternary{
  background: var(--quaternary-color);
}


.section-box h5 {
  margin: var(--small-gap) 0;
}


</style>
