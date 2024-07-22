<template>
    <section class="footer" :class="{ top: position, bottom: !position }">
        <div class="footer-link" v-for="(section, index) in sections" :key="index">
            <a class="link" @click="moveToSection(section.id)">{{ section.name }}</a>
            <pre class="link" v-if="index !== sections.length - 1">        /        </pre>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'FooterSection',
        data() {
            return {
                sections: [
                    {
                        name: 'About',
                        id: 'about-section'
                    },
                    {
                        name: 'Skills',
                        id: 'skills-section'
                    },
                    {
                        name: 'Portfolio',
                        id: 'portfolio-section'
                    },
                    {
                        name: 'Contact',
                        id: 'contact-section'
                    }
                ]
            }
        },
        props: {
            position: {
                type: Boolean,
                required: true
            }
        },
        methods: {
            moveToSection(section) {
                const contactSection = document.getElementById(section);
                contactSection.scrollIntoView({ behavior: 'smooth' });
            }
        }
    }
</script>

<style scoped>
    section.footer {
        width: 100%;
        padding: 20px 0;
        display: flex;
        justify-content: center;
        align-items: baseline;
    }
    
    div.footer-link {
        display: flex;
    }
    
    a.link, pre.link {
        color: var(--background);
        font-size: 18px;
        font-weight: 400;
        text-decoration: none;
    }
    a.link:hover {
        text-decoration: underline;
        cursor: pointer;
    }

    .top {
        position: absolute;
        top: 0;
    }

    .bottom {
        background: var(--primary);
    }

</style>