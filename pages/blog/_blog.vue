<template>
  <article
    v-if="blogPost"
    class="content"
  >
    <h1 class="article-title">{{ blogPost.title }}</h1>
    <h6
      class="article-date"
      v-if="blogPost.date"
    >{{ formatDate(blogPost.date) }}</h6>
    <div class="article-content" v-html="$md.render(blogPost.body)" />
  </article>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload }
    else
      return {
        blogPost: await require(`~/assets/content/blog/${params.blog}.json`)
      }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString("es") || ''
    }
  }
}
</script>
<style lang="postcss" scoped>
  .article-title{
    font-size: var(--extra-big-text-size);
    margin-top: var(--gap);
    text-transform: uppercase;
  }
  .article-date {
    font-size: var(--small-text-size);
    margin-bottom: var(--gap);
  }
  .article-content >>> p {
    margin-bottom: var(--gap);
    line-height: var(--big-text-size);
    text-align: justify;
  }

  .article-content >>> img {
    max-width: 100%;
  }
</style>