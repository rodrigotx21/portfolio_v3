<template>
    <section class="footer" :class="{ top: position, bottom: !position }">
        <div class="footer-link" v-for="(link, index) in links" :key="index">
            <a class="link" href="#">{{ link }}</a>
            <pre class="link" v-if="index !== links.length - 1">        /        </pre>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'FooterSection',
        data() {
            return {
                links: [
                    'About',
                    'Skills',
                    'Portfolio',
                    'Contact'
                ]
            }
        },
        props: {
            position: {
                type: Boolean,
                required: true
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
    }

    .top {
        position: absolute;
        top: 0;
    }

    .bottom {
        background: var(--primary);
    }

</style>