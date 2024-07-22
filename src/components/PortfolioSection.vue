<template>
    <section id="portfolio-section">
        <PortfolioDisplay />
        <h2 class="title">portfolio</h2>
    </section>
</template>

<script>
    import PortfolioDisplay from './PortfolioDisplay.vue'
    
    export default {
        name: 'PortfolioSection',
        components: {
            PortfolioDisplay
        }
    }
</script>

<style scoped>
    section#portfolio-section {
        padding: 80px;
        display: flex;
        justify-content: space-between;
    }
</style>