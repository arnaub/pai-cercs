<template>
  <div>
    <GreenBackground class="background-top"/>
    <GreenBackground class="background-bottom"/>
  </div>
</template>

<script>
import GreenBackground from '~/components/icons/fons-verd.svg?inline'

export default {
  components: {
    GreenBackground
  }
}
</script>

<style lang="postcss" scoped>
.background-top {
  position: absolute;
  top: 0;
  z-index: -1;
}

.background-bottom {
  transform: rotate(50deg);
  position: absolute;
  right: -50%;
  bottom: 0;
  width: 100vw;
  z-index: -1;
}
</style>
