<template>
    <div>
        <div class="hero">
            <div class="content">
                <div class="text-area">
                    <div class="text">
                        당신의 디스코드에<br />유니크한 재미를 더.
                    </div>
                </div>
                <div class="discord-logo" />
            </div>
        </div>
    </div>
</template>

<script lang="ts">
export default {
    name: 'Home',
}
</script>

<style scoped lang="scss">
.hero {
    background-image: url('~/assets/views/home/svg/bg1.svg');
    width: 100vw;
    min-height: 700px;
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;

    .content {
        display: flex;
        justify-content: space-between;
        gap: 75px;
        max-width: 1150px;
        width: 100%;
        .discord-logo {
            width: 305px;
            height: 350px;
            background-image: url('~/assets/views/home/svg/discord.svg');
        }
        .text-area {
            display: flex;
            flex-direction: column;
            .text {
                font-weight: 700;
                font-size: 90px;
                opacity: 0.7;
            }
        }
    }
}
</style>
