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
    <AboutSection />
    <SkillsSection />
    <FooterSection :position="bottom" />
    
    <!--
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

    h2.title {
        color: var(--title);
        font-size: 28px;
        font-style: italic;
        font-weight: 700;
    }
</style>