<template>
  <section class="about-section">
      <h2 class="title">portfolio</h2>
      <PortfolioDisplay />
  </section>
</template>

<script>
    import PortfolioDisplay from './PortfolioDisplay.vue'
    
    export default {
        name: 'AboutSection',
        componenets: {
            PortfolioDisplay
        }
    }
</script>

<style scoped>
  section.about-section {}

  h2#title {} /* global define outside */

  div.about-content {}

  p {}

  span.highlight {}
</style>