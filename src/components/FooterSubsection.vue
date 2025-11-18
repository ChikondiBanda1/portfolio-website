<template>
    <footer class="footer-subsection">
        <button class="button-4" @click="scrollToTop">
            <img class="icon" alt="Icon" src="https://c.animaapp.com/ujIwT5MJ/img/icon.svg" />
            <div class="text-wrapper-38">BACK TO TOP</div>
        </button>
        <div class="container-41 flex flex-row justify-center items-center gap-8">
            <div class="flex flex-row gap-3">
                <a class="socials"
                    href="mailto:chikondibanda257@gmail.com?subject=Hello&body=I%20would%20like%20to%20contact%20you."
                    target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20">
                        <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                            d="m18.333 5.833-7.492 4.773a1.667 1.667 0 0 1-1.675 0l-7.5-4.773" />
                        <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                            d="M16.666 3.333H3.333c-.92 0-1.667.747-1.667 1.667v10c0 .92.747 1.667 1.667 1.667h13.334c.92 0 1.666-.747 1.666-1.667V5c0-.92-.746-1.667-1.666-1.667Z" />
                    </svg>
                </a>

                <a class="socials" href="https://github.com/ChikondiBanda1" target="_blank" rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20">
                        <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                            d="M12.5 18.333V15a4 4 0 0 0-.833-2.917c2.5 0 5-1.666 5-4.583a4.503 4.503 0 0 0-.834-2.917 6.162 6.162 0 0 0 0-2.916s-.833 0-2.5 1.25a17.934 17.934 0 0 0-6.666 0c-1.667-1.25-2.5-1.25-2.5-1.25a5.765 5.765 0 0 0 0 2.916A4.502 4.502 0 0 0 3.333 7.5c0 2.917 2.5 4.583 5 4.583A3.93 3.93 0 0 0 7.5 15v3.333" />
                        <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                            d="M7.5 15c-3.759 1.667-4.167-1.667-5.833-1.667" />
                    </svg>

                </a>

                <a class="socials-last" href="https://www.linkedin.com/in/chikondi-banda/" target="_blank"
                    rel="noopener noreferrer">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20">
                        <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                            d="M13.334 6.667a5 5 0 0 1 5 5V17.5H15v-5.833a1.667 1.667 0 1 0-3.333 0V17.5H8.334v-5.833a5 5 0 0 1 5-5ZM5 7.5H1.667v10H5v-10ZM3.333 5a1.667 1.667 0 1 0 0-3.333 1.667 1.667 0 0 0 0 3.333Z" />
                    </svg>
                </a>
            </div>
        </div>

        <div class="container-42" />
        <div class="paragraph-6">
            <div class="text-wrapper-39">@2025 Chikondi Banda</div>
            <div class="text-wrapper-40">All Rights Reserved.</div>
        </div>
        <div class="text-wrapper-40">Designed and produced with Figma, Edited in Cursor.</div>
    </footer>
</template>

<script>
import { Icon } from '@iconify/vue';
export default {
    name: "FooterSubsection",
    components: {
        Icon,
    },
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }
    }
};
</script>

<style>
.footer-subsection {
    align-items: center;
    align-self: stretch;
    background-color: #2c3e50;
    display: flex;
    flex: 0 0 auto;
    flex-direction: column;
    gap: 24px;
    padding: 48px 24px;
    position: relative;
    width: 100%;
}

.footer-subsection .socials {
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 100%;
    margin-right: 12px;
}

.footer-subsection .socials-last {
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 100%;
}

.footer-subsection .button-4 {
    all: unset;
    box-sizing: border-box;
    height: 24px;
    position: relative;
    width: 139.3px;
}

.footer-subsection .button-4:hover {
    cursor: pointer;
}

.footer-subsection .button-4:hover .text-wrapper-38 {
    color: #ffffff;
}

.footer-subsection .button-4:hover .icon {
    filter: brightness(0) invert(1);
}

.footer-subsection .icon {
    height: 20px;
    left: 0;
    position: absolute;
    top: 2px;
    width: 20px;
}

.footer-subsection .text-wrapper-38 {
    color: #c9c4ba;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    left: 28px;
    letter-spacing: 0.49px;
    line-height: 24px;
    position: absolute;
    top: 0;
    white-space: nowrap;
}

.footer-subsection .container-41 {
    height: 32px;
    width: 100%;
}

.footer-subsection .container-42 {
    background: linear-gradient(180deg,
            rgba(0, 0, 0, 0) 0%,
            rgba(61, 90, 107, 1) 50%,
            rgba(0, 0, 0, 0) 100%);
    height: 1px;
    position: relative;
    width: 1181px;
}

.footer-subsection .paragraph-6 {
    align-items: center;
    display: flex;
    flex: 0 0 auto;
    gap: 4px;
    justify-content: center;
    position: relative;
    width: 1181px;
}

.footer-subsection .text-wrapper-39 {
    color: #c9c4ba;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: -0.15px;
    line-height: 20px;
    margin-top: -1.00px;
    position: relative;
    text-align: center;
    white-space: nowrap;
    width: fit-content;
}

.footer-subsection .text-wrapper-40 {
    color: #fffefe99;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: -0.15px;
    line-height: 20px;
    margin-top: -1.00px;
    position: relative;
    text-align: center;
    white-space: nowrap;
    width: fit-content;
}
</style>
