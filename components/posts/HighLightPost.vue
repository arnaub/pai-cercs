<template>
  <div class="article-hightligh">
    <div class="hightligh-media">
      <iframe class="video-player" src="https://www.youtube.com/embed/lnMqz5KOznw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="highlight-info">
      <nuxt-link :to="`blog/${highlightPost.slug}`">
        <h2 class="highlight-title">{{highlightPost.title}}</h2>
      </nuxt-link>
      <p class="highlight-description">{{highlightPost.description}}</p>
      <p class="highlight-description">{{highlightPost.description}}</p>
      <p class="highlight-description">{{highlightPost.description}}</p>
    </div>
  </div>
</template>

<script>

export default {
  props: ["highlightPost"],
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString("es") || ''
    }
  }
}
</script>

<style lang="postcss" scoped>
.article-hightligh {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: var(--gap);
    margin: var(--big-gap) 0;
  }

.hightligh-media {
  grid-column-start: 0;
  grid-column-end: span 7;
}

.highlight-info {
  grid-column-start: 8;
  grid-column-end: span 5;
}
.highlight-title {
  font-size: var(--big-text-size);
  margin-bottom: var(--small-gap)
}
.highlight-description {
  margin-bottom: var(--small-gap);
}

.video-player {
  width: 100%;
  height: 22vw;
}
</style>
