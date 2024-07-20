<template>
    <section class="landing-page">
        <FooterSection />
        <h1 class="main-title">HI, I'M RODRIGO</h1>
        <button @click="moveToContact()" id="connect-button">Connect with me!</button>
    </section>
</template>

<script>
    import FooterSection from './FooterSection.vue'
    
    export default {
        name: 'LandingPage',
        methods: {
            moveToContact() {
                // Logic for connecting goes here
            }
        },
        components: {
            FooterSection
        }
    }
</script>

<style scoped>
    section.landing-page {}
    
    h1#main-title {}

    button#connect-button {}
</style>