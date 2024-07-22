<template>
    <section id="about-section">
        <h2 class="title">about</h2>
        <div class="about-content">
            <p class="paragraph">enthusiastic about crafting <span class="highlight">user-friendly experiences</span> and tackling challenges with a collaborative spirit.</p>
            <p class="paragraph">ready to showcase <span class="highlight">my skills</span> through personal projects and open-source <span class="highlight">contributions</span>  .</p>
            <p class="paragraph">check out my portfolio and <span class="highlight">connect with me</span> to explore the possibilities!</p>
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
    section#about-section {
        padding: 80px;
        display: flex;
        justify-content: space-between;
    }

    div.about-content {
        width: 45vw;
        color: var(--text-transparent);
        text-align: justify;
        font-size: 28px;
        font-weight: 600;
    }

    p.paragraph {
        margin-bottom: 35px;
    }

    span.highlight {
        color: var(--text, #153448);
    }
</style>