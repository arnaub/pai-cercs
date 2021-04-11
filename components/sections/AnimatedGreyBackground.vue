<template>
  <div>
    <GreyBackground class="background-top"/>
    <GreyBackground class="background-bottom"/>
  </div>
</template>

<script>
import GreyBackground from '~/components/icons/fons-gris.svg?inline'

export default {
  components: {
    GreyBackground
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
