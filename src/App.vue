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
    data() {
        return {
            bottom: false
        }
    },
}
</script>

<template>
    <LandingPage />
    <FooterSection :position="bottom" />
    <!--<AboutSection />
    <SkillsSection />
    <FooterSection />
    <PortfolioSection />-->
</template>

<style>
    body {
        margin: 0;
        padding: 0;
        height: 100vh;
        background: var(--background);
    }
</style>