<template>
    <div>
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
                <div class="drawer-button">
                    <div @click="toggleDrawer" class="icon" />
                </div>
            </div>
        </div>
        <div class="drawer" @click="toggleDrawer" :class="{ open: drawer }">
            <div class="drawer-header">
                <div class="brand">
                    <div class="brand-icon" />
                    Uniquecode
                </div>
                <div class="icon" />
            </div>
            <nuxt-link to="/projects">프로젝트</nuxt-link>
            <nuxt-link to="/members">멤버</nuxt-link>
            <nuxt-link to="/recruit">채용</nuxt-link>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
    data: () => ({
        drawer: false,
    }),
    methods: {
        toggleDrawer() {
            this.drawer = !this.drawer
        },
    },
}
</script>

<style scoped lang="scss">
.drawer {
    position: fixed;
    left: 0;
    top: 0;
    height: 100vh;
    width: 100vw;
    background: #fff;
    display: none;
    flex-direction: column;
    box-sizing: border-box;

    .drawer-header {
        .icon {
            background-image: url('~/assets/svg/icons/close.svg');
            width: 40px;
            height: 40px;
            background-size: cover;
            cursor: pointer;
        }

        border-bottom: 1px solid #f0f0f0;

        .brand {
            font-size: 25px;
        }

        align-items: center;
        display: flex;
        justify-content: space-between;
        padding: 10px;
    }

    a {
        padding: 10px 10px 10px 15px;
        box-sizing: border-box;
        color: #000;
        text-decoration: none;

        &:hover {
            color: #6b6b6b;
        }
    }

    &.open {
        display: flex;
    }
}

.container {
    width: 100%;
    justify-content: center;
    padding-left: 30px;
    padding-right: 30px;
    box-sizing: border-box;

    & > div {
        max-width: 1000px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .drawer-button {
            display: block;

            .icon {
                background-image: url('~/assets/svg/icons/menu.svg');
                width: 40px;
                height: 40px;
                background-size: cover;
                cursor: pointer;
            }

            .brand-icon {
                background-image: url('~/assets/svg/icons/menu.svg');
                width: 40px;
                height: 40px;
                background-size: cover;
                cursor: pointer;
            }

            @media screen and (min-width: 768px) {
                display: none;
            }
        }

        .links-area {
            @media screen and (max-width: 768px) {
                display: none;
            }

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
