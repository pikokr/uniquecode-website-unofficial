<template>
  <div>
    <DefaultHeader no-spacing />
    <Nuxt />
    <DefaultFooter />
  </div>
</template>
<script lang="ts">
import DefaultHeader from '@/components/layouts/default/components/DefaultHeader.vue'
import DefaultFooter from '~/components/layouts/default/components/DefaultFooter.vue'
export default {
  components: { DefaultFooter, DefaultHeader },
}
</script>
