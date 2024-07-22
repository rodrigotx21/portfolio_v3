<template>
    <section id="contact-section">
        <h2 class="title">contact</h2>
        <form class="contact-form">
            <input type="text" placeholder="name" v-model="name" />
            <input type="email" placeholder="email" v-model="email" />
            <textarea placeholder="message" v-model="message"></textarea>
            <button  type="submit">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="33" viewBox="0 0 32 33" fill="none">
                    <path d="M8.70357 31.1094V25.1243C8.70357 24.4489 9.36063 23.9686 10.0042 24.1737L16.8895 26.3675C17.7244 26.6335 17.8354 27.7695 17.0678 28.1921L10.1825 31.9834C9.51758 32.3495 8.70357 31.8684 8.70357 31.1094Z" fill="#153448"/>
                    <path d="M10.565 21.2102C10.2079 21.5789 9.6705 21.7092 9.18413 21.5451L1.84411 19.0681C-0.231542 18.3356 -0.40998 15.4695 1.55877 14.4851L28.2077 1.16063C30.0762 0.226368 32.1967 1.86556 31.7632 3.90916L27.3278 24.819C27.0189 26.2753 25.5113 27.1385 24.099 26.6678L13.8973 23.2595C13.2111 23.0303 12.9894 22.1698 13.4794 21.6375L21.7186 12.6863C22.2631 12.0644 22.6648 11.4107 22.0429 10.8663C21.421 10.3218 20.6073 10.7822 20.0628 11.4041L10.565 21.2102Z" fill="#153448"/>
                </svg>
                Send
            </button>
        </form>
    </section>
</template>

<script>
    export default {
        name: 'ContactSection',
        data() {
        return {
                name: '',
                email: '',
                message: ''
            }
        },
    }
</script>

<style scoped>
    section#contact-section {
        padding: 80px;
        padding-top: 0;
        display: flex;
        justify-content: space-between;
    }

    .contact-form {
        display: flex;
        flex-direction: column;
        gap: 5px;
        width: 50vw;
    }

    input, textarea {
        padding: 10px;

        color: var(--text-transparent);
        font-size: 18px;
        font-weight: 400;

        background: none;
        border-radius: 10px;
        border: 2px solid var(--text-transparent, rgba(21, 52, 72, 0.50));
    }

    textarea {
        height: 100px;
        resize: none;
    }

    button {
        padding: 15px;

        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;

        color: var(--primary);
        font-size: 18px;
        font-weight: 600;

        border: none;
        border-radius: 12px;
        border: 2px solid var(--primary);
    }
</style>