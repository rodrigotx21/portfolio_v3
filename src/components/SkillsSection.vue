<template>
    <section class="skills-section">
        <p v-for="skill in skills" class="skill">{{ skill }}</p>
        <div class="frame"></div>
    </section>
</template>

<script>
    export default {
        name: 'SkillsSection',
        data() {
            return {
                skills: [
                    "HTML", 
                    "CSS",
                    "JAVASCRIPT",
                    "VUE.JS",
                    "C",
                    "PYTHON"
                ]
            };
        }
    }
</script>

<style scoped>
    section.skills-section {
        width: 100%;
        height: 230px;

        display: flex;
        justify-content: center;
        align-items: center;
        gap: 60px;

        border: 2px solid var(--text-transparent, var(--text-transparent));
        border-left: none;
        border-right: none;
        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
    }

    p.skill {
        font-family: Bungee;
        font-size: 48px;
        font-weight: 400;
        color: var(--text-transparent, rgba(21, 52, 72, 0.50));
    }

    div.frame {
        position: absolute;
        z-index: 10;

        width: 100%;
        height: 230px;
        background: linear-gradient(90deg, var(--background) 0%, rgba(245, 239, 230, 0.00) 45%, var(--background) 100%);
    }
</style>