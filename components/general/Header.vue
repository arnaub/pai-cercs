<template>
  <header class="header">
    <nav class="navigation">
      <ul class="menu">
        <li class="menu__item">
          <nuxt-link class="btn block" to="/">Home</nuxt-link>
        </li>
        <li class="menu__item">
          <nuxt-link class="btn block" to="/blog">Notícies</nuxt-link>
        </li>
        <li class="menu__item">
          <nuxt-link class="btn block" to="/documents">Documents</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="postcss" scoped>
.header {
  width: 100%;
  height: 60px;
  position: sticky;
  background: rgba(255,255,255,0.5);
}

.menu {
  display: flex;
  justify-content: flex-end;
}

.menu__item {
  display: inline-block;
  height: 60px;
  line-height: 60px;
  font-size: 1em;
  padding: 0 2em;
}

.nuxt-link-exact-active {
  color: var(--primary-color);
  &:after
}
</style>
