<template>
    <img
        v-for="e in fireworks"
        :src="fireworksSprite"
        :style="{
            left: e.left + 'px',
            top: e.top + 'px',
            width: e.width + 'px',
            rotate: e.rotate + 'deg',
        }"
        class="absolute animate__animated animate__fadeIn animate__zoomIn z-0"
    />
</template>

<script>
import fireworksSprite from "../../assets/fireworks.svg";

export default {
    computed: {
        fireworks() {
            return Array.from({ length: 20 }).map(() => ({
                top: Math.floor(Math.random() * 300) + 20,
                left: Math.floor(Math.random() * 500) + 50,
                width: Math.floor(Math.random() * 40),
                rotate: Math.floor(Math.random() * 360),
            }));
        },
    },
    data() {
        return {
            fireworksSprite,
        };
    },
};
</script>

<style scoped>
@keyframes fireworks {
    0% {
        transform: scale(0);
        opacity: 80%;
    }
    80% {
        opacity: 80%;
    }
    100% {
        transform: scale(1.8);
        opacity: 10%;
    }
}

img {
    animation: fireworks 1.5s ease-in-out infinite;
    z-index: -1;
}
</style>
