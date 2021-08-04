<template>
    <div>
        <div style="position: absolute; top: 25px; left: 0; width: 100vw">
            <Header />
        </div>
        <Home />
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Home from '~/components/views/Home.vue'
import Header from '~/components/Header.vue'

export default Vue.extend({
    components: { Header, Home },
})
</script>
