<template>
  <header
    class="py-6 ease-in-out sticky top-0 transition-colors"
    :class="{ 'bg-white': !view.atTopOfPage }"
  >
    <div class="container mx-auto">test</div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DefaultHeader',

  data() {
    return {
      view: {
        atTopOfPage: true,
      },
    }
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
  },

  methods: {
    handleScroll() {
      if (window.pageYOffset > 0) {
        if (this.view.atTopOfPage) this.view.atTopOfPage = false
      } else {
        !this.view.atTopOfPage && (this.view.atTopOfPage = true)
      }
    },
  },
})
</script>
