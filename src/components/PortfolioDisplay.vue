<template>
    <div class="portfolio">
        <img :src="pages[active_page].src" 
            :alt="pages[active_page].title"
            :title="pages[active_page].title"
            @click="openLink(pages[active_page].link)"
        >

        <DisplayController id="controller"
            :active_page="active_page"
            :pages="pages"
            @change-page="handleChangePage"
        />
    </div>
</template>

<script>
import DisplayController from './DisplayController.vue'

export default {
    components: {
        DisplayController
    },
    data() {
        return {
            active_page: 0,
            pages: [
                { 
                    link: "https://rodrigotx21.github.io/mortgage-repayment-calculator-main/",
                    src: "src/assets/portfolio/mortage-payment-calculator.png", 
                    title: "Mortgage Payment Calculator" 
                },
                { 
                    link: "https://rodrigotx21.github.io/newsletter-sign-up-with-success-message-main/",
                    src: "src/assets/portfolio/newsletter-sign-up.png", 
                    title: "Newsletter Sign Up" 
                },
                { 
                    link: null,
                    src: "src/assets/portfolio/old_portfolio.png", 
                    title: "Old Portfolio" 
                },
                { 
                    link: "https://rodrigotx21.github.io/qr-code-component-main/",
                    src: "src/assets/portfolio/qr-code-component.png", 
                    title: "QR Code Component" 
                },
                { 
                    link: "https://rodrigotx21.github.io/simple-coffee-listing/",
                    src: "src/assets/portfolio/simple-coffee-listing.png", 
                    title: "Simple Coffee Listing" 
                }
            ],
            intervalId: null // Store the interval ID for clearing later
        }
    },
    methods: {
        handleChangePage(index) {
            this.active_page = (index + this.pages.length) % this.pages.length;
            // Clear the existing interval
            clearInterval(this.intervalId);
            // Start a new interval
            this.startAutoChangePage();
        },
        startAutoChangePage() {
            this.intervalId = setInterval(() => {
                this.handleChangePage(this.active_page + 1);
            }, 5000);
        },
        openLink(url) {
            if (url != null) {
                window.open(url, '_blank');
            }
        }
    },
    mounted() {
        this.startAutoChangePage();
    },
    beforeDestroy() {
        // Clear the interval when the component is destroyed
        if (this.intervalId) {
            clearInterval(this.intervalId);
        }
    }
}
</script>

<style scoped>
    div.portfolio {
        width: 50vw;
        height: 30vw;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 12px;
        position: relative; /* Make this a positioning context */
    }
    
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        position: absolute;
        top: 0;
        left: 0;
    }
    img:hover {
        cursor: pointer;
    }
</style>