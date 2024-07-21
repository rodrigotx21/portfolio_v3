<script>
import LandingPage from './components/LandingPage.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import FooterSection from './components/FooterSection.vue'
import PortfolioDisplay from './components/PortfolioDisplay.vue'
import './styles/variables.css'
import './styles/material-symbols-outlined.css'

export default {
    components: {
        LandingPage,
        AboutSection,
        SkillsSection,
        FooterSection,
        PortfolioDisplay
    },
}
</script>

<template>
    <!--<LandingPage />
    <AboutSection />
    <SkillsSection />
    <FooterSection />-->
    <PortfolioDisplay />
</template>

<style scoped>
</style>