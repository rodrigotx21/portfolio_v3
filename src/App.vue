<script>
import LandingPage from './components/LandingPage.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import FooterSection from './components/FooterSection.vue'
import DisplayControler from './components/DisplayControler.vue'
import './styles/variables.css'

export default {
    components: {
        LandingPage,
        AboutSection,
        SkillsSection,
        FooterSection,
        DisplayControler
    },
    data() {
        return {
            dots: 3
        }
    }
}
</script>

<template>
    <!--<LandingPage />
    <AboutSection />
    <SkillsSection />
    <FooterSection />-->
    <DisplayControler :dots="dots"/>
</template>

<style scoped>
</style>