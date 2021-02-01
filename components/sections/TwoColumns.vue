<template>
  <section class="two-columns">
    <div class="column column-left">
      <h2 class="column-title">Indigenous Cultural Safety & Cultural Humility</h2>
      <p class="column-paragraph">{{description}}</p>
      <p class="column-paragraph">{{description}}</p>
      <p class="column-paragraph">{{description}}</p>
    </div>
    <div class="column column-right">
      <p class="column-paragraph">{{description}}</p>
      <p class="column-paragraph">{{description}}</p>
      <p class="column-paragraph">{{description}}</p>
    </div>
  </section>
</template>

<script>

export default {
  props: ["title", "description"],
}
</script>

<style lang="postcss" scoped>
.two-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}

.column {
  box-sizing: border-box;
  width: 100%;
  padding: var(--gap);
  background: var(--primary-color);
}

.column-paragraph {
  margin-bottom: var(--small-gap);
}

.column-right {
  background: var(--quaternary-color);
}

.column-title {
  margin-bottom: var(--small-gap);
  font-size: var(--extra-big-text-size);
}

</style>
