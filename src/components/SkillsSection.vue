<template>
    <section class="skills-section">
        <p v-for="skill in skills" class="skill">{{ skill }}</p>
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
                    "PYTHON",
                    "C"
                ]
            };
        }
    }
</script>

<style scoped>
</style>