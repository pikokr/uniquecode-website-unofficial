<template>
  <div class="container">
    <div>
      <nuxt-link to="/" class="logo-area">
        <div class="logo" />
        <span class="logo-text">Uniquecode</span>
      </nuxt-link>
      <div class="links-area">
        <nuxt-link to="/projects">프로젝트</nuxt-link>
        <nuxt-link to="/members">멤버</nuxt-link>
        <nuxt-link to="/recruit">채용</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped lang="scss">
.container {
  width: 100%;
  position: absolute;
  top: 25px;
  display: flex;
  justify-content: center;
  & > div {
    max-width: 1000px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .links-area {
      display: flex;
      gap: 50px;
      a {
        text-decoration: none;
        color: #000;
        font-size: 25px;
      }
    }
    .logo-area {
      display: flex;
      gap: 20px;
      text-decoration: none;
      align-items: center;
      color: #000;

      .logo-text {
        font-weight: 700;
        font-size: 25px;
      }
      .logo {
        width: 50px;
        height: 50px;
        background-size: cover;
        background-image: url('~/assets/svg/logo.svg');
      }
    }
  }
}
</style>
