<template>
    <div class="container">
        <img class="arrow" :src="arrowBackward" />
    </div>
    <div class="container pages">
        <img class="dot" :src="dot" v-for="index in dots" :key="index" />
    </div>
    <div class="container">
        <img class="arrow" :src="arrowForeward" />
    </div>
</template>

<script>
    export default {
        name: 'DisplayControler',
        data() {
            return {
                arrowBackward: 'src/assets/arrow_backward.svg',
                arrowForeward: 'src/assets/arrow_forward.svg',
                dot: 'src/assets/dot.svg'
            };
        },
        props: {
            dots: {
                type: Number,
                required: true
            }
        }
    }
</script>

<style scoped>
    div.container {
        heigth: fit-content;
        width: fit-content;
        padding: 1px;
        border-radius: 50px;
        background: var(--text-transparent);
    }
</style>