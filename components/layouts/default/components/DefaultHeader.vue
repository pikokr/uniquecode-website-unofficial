<template>
  <header
    class="py-6 header-container ease-in-out bg-white sticky top-0 transition-colors bg-white bg-opacity-50"
  >
    <div class="container px-4 mx-auto">test</div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DefaultHeader',
})
</script>

<style scoped>
.header-container {
  backdrop-filter: blur(20px);
}
</style>
