<template>
  <div>
    <Header />
    <div class="hero">asdf</div>
  </div>
</template>

<script lang="ts">
import Header from '~/components/Header.vue'
export default {
  name: 'Home',
  components: { Header },
}
</script>

<style scoped lang="scss">
.hero {
  background-image: url('~/assets/views/home/svg/bg1.svg');
  width: 100vw;
  height: 700px;
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
