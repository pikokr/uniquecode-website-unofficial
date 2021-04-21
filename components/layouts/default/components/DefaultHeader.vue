<template>
  <div>
    <header class="header-container">
      <div class="lg:w-2/3 px-6 mx-auto flex items-center">
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
          <nuxt-link v-for="(x, y) in nav" :key="y" :to="x.to">{{
            x.text
          }}</nuxt-link>
        </div>
        <div class="md:hidden">
          <v-btn icon x-large outlined @click.stop="drawer = true">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </div>
      </div>
    </header>
    <v-navigation-drawer v-model="drawer" right temporary absolute>
      <div class="flex p-4 pb-0">
        <div class="flex gap-2 items-center">
          <img
            :src="require('@/assets/img/logo.png')"
            class="w-8 h-8"
            alt="Logo"
          />
          <span class="text-xl font-bold">Uniquecode</span>
        </div>
        <v-spacer />
        <v-btn icon @click.stop="drawer = false">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </div>
      <v-list dense nav>
        <v-list-item v-for="(x, y) in nav" :key="y" :to="x.to">
          <v-list-item-content>
            <v-list-item-title>{{ x.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'DefaultHeader',
  data: () => ({
    drawer: false,
    nav: [
      {
        text: '프로젝트',
        to: '/projects',
      },
      {
        text: '멤버',
        to: '/members',
      },
      {
        text: '채용',
        to: '/jobs',
      },
    ],
  }),
})
</script>

<style scoped lang="scss">
.header-container {
  backdrop-filter: blur(20px);
  @apply md:py-4 py-4 lg:py-6 ease-in-out bg-white sticky top-0 transition-colors bg-white bg-opacity-50;
}
.items-area {
  a {
    @apply text-3xl font-bold;
  }
  @apply md:flex hidden gap-16;
}
</style>
