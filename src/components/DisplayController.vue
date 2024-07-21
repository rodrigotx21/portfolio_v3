<template>
    <div class="controler">
        <button class="container arrow"  @click="$emit('change-page', active_page - 1)">
            <div class="material-symbols">chevron_left</div>
        </button>
        <div class="container">
            <div class="material-symbols"
                v-for="index in pages.length"
                :class="{ filled: index == active_page + 1 }" 
                :key="index"
            >fiber_manual_record</div>
        </div>
        <button class="container arrow" @click="$emit('change-page', active_page + 1)">
            <div class="material-symbols">chevron_right</div>
        </button>
    </div>
</template>

<script>
    export default {
        name: 'DisplayControler',
        props: {
            active_page: {
                type: Number,
                required: true
            },
            pages: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style scoped>
    div.controler {
        display: flex;
        gap: 2px;
    }

    div.container, button.container {
        height: fit-content;
        width: fit-content;
        padding: 2px;

        display: flex;

        border: none;
        border-radius: 50px;
        background: var(--text-transparent);
    }

    button.arrow:hover {
        cursor: pointer;
        background: var(--text);
    }
    button.arrow:hover > .material-symbols {
        color: var(--background);
    }
</style>