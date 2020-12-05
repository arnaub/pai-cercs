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
  display: flex;
  flex-direction: column;
  width: 100px;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  background: rgba(255,255,255,0.5);
}

.menu__item {
  display: block;
  height: 60px;
  line-height: 60px;
  font-size: 1em;
}

.nuxt-link-exact-active {
  color: var(--quinary-color);
  &:after
}
</style>
