<template>
  <header
    class="py-6 header-container ease-in-out bg-white sticky top-0 transition-colors bg-white bg-opacity-50"
  >
    <div class="container px-6 mx-auto flex items-center">
      <nuxt-link to="/" class="flex gap-4 items-center">
        <img
          :src="require('@/assets/img/logo.png')"
          class="w-12 h-12"
          alt="Logo"
        />
        <span class="text-3xl font-bold">Uniquecode</span>
      </nuxt-link>
      <div class="flex-grow" />
      <div class="items-area">
        <nuxt-link to="/projects">프로젝트</nuxt-link>
        <nuxt-link to="/projects">멤버</nuxt-link>
        <nuxt-link to="/projects">채용</nuxt-link>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DefaultHeader',
})
</script>

<style scoped lang="scss">
.header-container {
  backdrop-filter: blur(20px);
}
.items-area {
  a {
    @apply text-3xl font-bold;
  }
  @apply flex gap-16;
}
</style>
