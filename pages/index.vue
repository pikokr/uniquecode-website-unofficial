<template>
  <div>
    <div
      class="absolute top-0 w-full h-2/3"
      style="background: rgba(112, 112, 112, 0.22)"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        style="max-height: 100%"
        viewBox="0 0 1869.772 684.634"
        class="absolute top-0 w-full h-2/3"
      >
        <path
          d="M1118.042-12l274.635,276.7L1833.01-12l105.726,276.7L1553.565,475.53,1791.246,671.4,937.323,455.524,621.611,666.362,357.747,289.474,745.642,32.46,70.127,257.61l44.785,408.752"
          transform="translate(-69.586 12.747)"
          fill="none"
          stroke="#707070"
          stroke-linecap="round"
          stroke-width="1"
          opacity="0.223"
          class="hero-svg"
        />
      </svg>
      <div class="lg:w-2/3 px-6 mx-auto mt-12 mt-36">
        <div class="flex justify-center gap-4">
          <div class="text-7xl font-bold opacity-70">
            <p>당신의 디스코드에</p>
            <p>유니크한 재미를 더.</p>
          </div>
          <fa-icon
            style="font-size: 200px; color: #738adb"
            :icon="['fab', 'discord']"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-path {
  animation: dash 5s linear alternate infinite;
}

@keyframes dash {
  from {
    stroke-dashoffset: 822;
  }
  to {
    stroke-dashoffset: 0;
  }
}
</style>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>
