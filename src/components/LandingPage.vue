<template>
    <!-- Background from https://superdesigner.co/ -->
    <section id="landing-page">
        <FooterSection :position="top" />
        <h1 class="main-title">HI, I'M RODRIGO</h1>
        <button @click="moveToSection('contact-section')" id="connect-button">Connect with me!</button>
    </section>
</template>

<script>
    import FooterSection from './FooterSection.vue'
    
    export default {
        name: 'LandingPage',
        data() {
            return {
                top: true
            };
        },
        methods: {
            moveToSection(section) {
                const contactSection = document.getElementById(section);
                contactSection.scrollIntoView({ behavior: 'smooth' });
            }
        },
        components: {
            FooterSection
        }
    }
</script>

<style scoped>
    section#landing-page {
        display: flex;
        height: 600px;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 44px;
        
        background: linear-gradient(180deg, rgba(245, 239, 230, 0.00) 77.19%, #F5EFE6 100%), 
                    url("../assets/background.jpeg") lightgray 50% / cover no-repeat;

    }
    
    h1.main-title {
        font-size: 146px;
        font-weight: 700;
        color: var(--primary);
    }

    button#connect-button {
        padding: 20px 50px;

        border: none;
        border-radius: 50px;
        background: var(--background);

        color: var(--primary);
        font-size: 20px;
        font-style: normal;
        font-weight: 500;
    }
    button#connect-button:hover {
        background: var(--primary);
        color: var(--background);
        cursor: pointer;
    }
</style>