<template>
  <main
    v-if="documentPosts"
    class="main"
  >
    <h1 class="title">Documents</h1>
    <ul>
      <li
        v-for="(documentPost, index) in documentPosts"
        :key="index"
      >{{documentPost.title}}</li>
    </ul>
  </main>
</template>
<script>
export default {
  computed: {
    documentPosts() {
      return this.$store.state.documentPosts
    }
  }
}
</script>
