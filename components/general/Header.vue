<template>
  <header class="header">
    <nav class="navigation">
      <img src="img/logo.jpg" class="logo" />
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
      <ul class="social-media">
        <li class="social-item"><a class="social-link" target="blank" href="https://twitter.com/pcercs"><font-awesome-icon :icon="['fab', 'twitter']" /></a></li>
        <li class="social-item"><a class="social-link" target="blank" href="https://www.instagram.com/plataformacercs/"><font-awesome-icon :icon="['fab', 'instagram']" /></a></li>
        <li class="social-item"><a class="social-link" target="blank" href="https://www.youtube.com/channel/UCphzBQDH2A1ee65fVefJabQ/featured"><font-awesome-icon :icon="['fab', 'youtube']" /></a></li>
      </ul>
    </nav>
    <div class="color-wrapper">
      <ColorModePicker />
    </div>
  </header>
</template>

<script>
import ColorModePicker from '~/components/general/ColorModePicker.vue'

export default {
  name: 'Header',
  components: {
    ColorModePicker
  }
}
</script>

<style lang="postcss" scoped>
.header {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  width: 0;
  overflow: hidden;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  background: white;
  @media only screen and (min-width: 992px) {
    width: 120px;
  }
}
.header.open {
  width: 100%;
}

.logo {
  display: block;
  width: var(--gap);
  margin: var(--small-gap) auto;
}

.menu {
  width: 100%;
  box-sizing: border-box;
}

.menu__item {
  display: block;
  margin-bottom: var(--extra-small-gap);
  font-size: 1.2rem;
  text-align: center;
}

.nuxt-link-exact-active {
  color: var(--highlight);
  &:after
}

.social-media {
  margin-top: var(--big-gap);
}
.social-item {
  margin-bottom: var(--small-gap);
  text-align: center;
}

.social-link {
  width: 2em;
  height: 2em;
  font-size: 1.8em;
  margin: 0 auto;
  display: block;
}

.color-wrapper {
  width: 50%;
  position: absolute;
  bottom: var(--small-gap);
  left: 50%;
  transform: translateX(-50%);
}
</style>
