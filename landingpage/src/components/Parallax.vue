<!-- Parallax.vue -->
<template>
    <div class="parallax-container" @mousemove="handleMouseMove">
        <div class="parallax-layer" :style="{ transform: `translate(${x}px, ${y}px)` }">
            HELLO WORLD
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            x: 0,
            y: 0,
        };
    },
    methods: {
        handleMouseMove(event) {
            // Update the x and y data properties based on mouse movement
            this.x = (event.clientX / window.innerWidth) * 100 - 50;
            this.y = (event.clientY / window.innerHeight) * 100 - 50;
        },
    },
};
</script>

<style scoped>
.parallax-container {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    position: relative;
}

.parallax-layer {
    width: 100%;
    height: 100%;
    background-image: url('');
    background-size: cover;
    background-position: center;
    position: absolute;
    transition: transform 0.3s ease-out;
}
</style>
