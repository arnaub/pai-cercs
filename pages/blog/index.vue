<template>
  <main
    v-if="blogPosts"
    class="content"
  >
    <h1 class="articles-title">Notícies</h1>
    <div class="articles-list">
      <div class="article-hightligh">
        <iframe class="hightligh-media" src="https://www.youtube.com/embed/lnMqz5KOznw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <nuxt-link :to="`blog/${hightlighPost.slug}`">
          <h2>{{hightlighPost.title}}</h2>
          <p>{{hightlighPost.description}}</p>
        </nuxt-link>
      </div>
      <ArticleItem
        v-for="(blogPost, index) in blogPosts"
        :key="index"
        :post="blogPost"
        class="article"
      />
      <ArticleItem
        v-for="(blogPost, index) in blogPosts"
        :key="index"
        :post="blogPost"
        class="article"
      />
      <ArticleItem
        v-for="(blogPost, index) in blogPosts"
        :key="index"
        :post="blogPost"
        class="article"
      />
      <ArticleItem
        v-for="(blogPost, index) in blogPosts"
        :key="index"
        :post="blogPost"
        class="article"
      />
      <ArticleItem
        v-for="(blogPost, index) in blogPosts"
        :key="index"
        :post="blogPost"
        class="article"
      />
    </div>
  </main>
</template>
<script>

import ArticleItem from '~/components/posts/ArticleItem';

export default {
  components: {
    ArticleItem
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    },
    hightlighPost() {
      return this.$store.state.blogPosts[0];
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

  .articles-title {
    font-size: var(--extra-big-text-size);
    text-transform: uppercase;
    margin: var(--gap) 0;
  }

  .articles-list {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: var(--small-gap);
  }

  .article-hightligh {
    grid-column-start: 1;
    grid-column-end: span 2;
    grid-row-start: 1;
    grid-row-end: span 2;
  }

  .hightligh-media {
    width: 100%;
    height: 30vh;
    margin-bottom: var(--small-gap);
  }

  .article {
    height: 20vh;
    background: rgba(0, 0, 0, 0.4);
  }
</style>


