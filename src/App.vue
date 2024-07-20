<script>
import LandingPage from './components/LandingPage.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import FooterSection from './components/FooterSection.vue'

export default {
    components: {
        LandingPage,
        AboutSection,
        SkillsSection,
        FooterSection
    }
}
</script>

<template>
    <LandingPage />
    <AboutSection />
    <SkillsSection />
    <FooterSection />
</template>

<style scoped>
</style>