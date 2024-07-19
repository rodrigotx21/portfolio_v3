<template>
    <section class="landing-page">
        <h1 class="main-title">HI, I'M RODRIGO</h1>
        <button @click="moveToContact()" id="connect-button">Connect with me!</button>
    </section>
</template>

<script>    
    export default {
        name: 'LandingPage',
        methods: {
            moveToContact() {
                // Logic for connecting goes here
            }
        }
    }
</script>

<style scoped>
    section.landing-page {}
    
    h1#main-title {}

    button#connect-button {}
</style>