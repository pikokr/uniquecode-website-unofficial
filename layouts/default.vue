<template>
  <div>
    <DefaultHeader />
    <Nuxt />
  </div>
</template>
<script lang="ts">
import DefaultHeader from '@/components/layouts/default/components/DefaultHeader.vue'
export default {
  components: { DefaultHeader },
}
</script>
