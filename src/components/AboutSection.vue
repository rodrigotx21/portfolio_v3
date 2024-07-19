<template>
    <section class="about-section">"
        <h2 class="title">about</h2>
        <div class="about-content">
            <p>enthusiastic about crafting <span class="highlight">user-friendly experiences</span> and tackling challenges with a collaborative spirit.</p>
            <p>ready to showcase <span class="highlight">my skills</span> through personal projects and open-source <span class="highlight">contributions</span>  .</p>
            <p>check out my portfolio and <span class="highlight">connect with me</span> to explore the possibilities!</p>
        </div>
    </section>
</template>

<script>    
    export default {
        name: 'AboutSection',
        methods: {
            moveToContact() {
                // Logic for connecting goes here
            }
        }
    }
</script>

<style scoped>
    section.about-section {}

    h2#title {}

    div.about-content {}

    p {}

    span.highlight {}
</style>