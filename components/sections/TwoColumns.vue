<template>
  <section class="columns">
    <h2 class="column-title">Indigenous Cultural Safety & Cultural Humility</h2>
    <div class="two-columns">
      <div class="column column-left">
        <p class="column-paragraph">{{description}}</p>
        <p class="column-paragraph">{{description}}</p>
        <p class="column-paragraph">{{description}}</p>
      </div>
      <div class="column column-right">
        <p class="column-paragraph">{{description}}</p>
        <p class="column-paragraph">{{description}}</p>
        <p class="column-paragraph">{{description}}</p>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  props: ["title", "description"],
}
</script>

<style lang="postcss" scoped>
.columns {
  margin: var(--big-gap) 0;
}
.two-columns {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--gap)
}

.column {
  box-sizing: border-box;
  width: 100%;
  text-align: justify;
}

.column-paragraph {
  margin-bottom: var(--small-gap);
  line-height: 1.5;
  font-size: var(--text-size);
}

.column-title {
  margin-bottom: var(--small-gap);
  font-size: var(--extra-big-text-size);
}

</style>
