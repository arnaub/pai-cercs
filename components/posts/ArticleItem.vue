<template>
  <div class="article-info">
    <h3 class="article-title">
      <nuxt-link
        :to="`blog/${post.slug}`"
      >
        {{ post.title }}
      </nuxt-link>
    </h3>
    <h6
      v-if="post.date"
      class="article-date"
    >{{ formatDate(post.date) }}</h6>
  </div>
</template>

<script>

export default {
  props: ["post"],
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString("es") || ''
    }
  }
}
</script>

<style lang="postcss" scoped>
  .article {
    height: 20vh;
    background: rgba(0, 0, 0, 0.4);
  }
</style>
