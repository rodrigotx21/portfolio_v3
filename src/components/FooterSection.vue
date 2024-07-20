<template>
    <section class="footer">
        <div class="footer-link" v-for="(link, index) in links" :key="index">
            <a class="link">{{ link }}</a>
            <pre class="link" v-if="index !== links.length - 1">  •  </pre>
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
            bgTransparent: {
                type: Boolean,
                required: true
            }
        }
    }
</script>