<template>
  <section class="highlight">
    <h2 class="highlight-title">{{text}}</h2>
  </section>
</template>

<script>

export default {
  props: ["text"]
}
</script>

<style lang="postcss" scoped>
.highlight {
  width: 100%;
  height: 60vh;
  margin: var(--big-gap) 0;
  padding: var(--gap);
  color: white;
  background: var(--text-color-secondary);
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.highlight-title {
  font-size: var(--big-text-size);
  line-height: var(--extra-big-text-size);
  text-align: center;
}
.highlight-title::before, .highlight-title::after {
  content: '';
  display: block;
  height: 2px;
  width: 200px;
  background: var(--quinary-color);
  margin: var(--gap) auto;
}

</style>
