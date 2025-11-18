<template>
    <div class="section-subsection h-screen">
        <div class="rectangle"></div>
        <div class="div">
            <div class="container-2" />
            <div class="container-3" />
        </div>
        <div class="container-4">
            <div class="container-5">
                <div class="container-6">
                    <div class="paragraph">
                        <div class="hello-i-m">Hello, I&#39;m</div>
                    </div>
                    <div class="heading">
                        <div class="text-wrapper">Chikondi Banda</div>
                    </div>
                </div>
                <div class="div-wrapper">
                    <p class="p">Software Developer / Data Analyst</p>
                </div>
                <div class="creating-beautiful-wrapper">
                    <p class="creating-beautiful">
                        Designing and building solutions to business and community
                        problems.
                    </p>
                </div>
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

                    <a class="socials" href="https://github.com/ChikondiBanda1" target="_blank"
                        rel="noopener noreferrer">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20">
                            <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                                d="M12.5 18.333V15a4 4 0 0 0-.833-2.917c2.5 0 5-1.666 5-4.583a4.503 4.503 0 0 0-.834-2.917 6.162 6.162 0 0 0 0-2.916s-.833 0-2.5 1.25a17.934 17.934 0 0 0-6.666 0c-1.667-1.25-2.5-1.25-2.5-1.25a5.765 5.765 0 0 0 0 2.916A4.502 4.502 0 0 0 3.333 7.5c0 2.917 2.5 4.583 5 4.583A3.93 3.93 0 0 0 7.5 15v3.333" />
                            <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                                d="M7.5 15c-3.759 1.667-4.167-1.667-5.833-1.667" />
                        </svg>

                    </a>

                    <a class="socials" href="https://www.linkedin.com/in/chikondi-banda/" target="_blank"
                        rel="noopener noreferrer">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20">
                            <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.667"
                                d="M13.334 6.667a5 5 0 0 1 5 5V17.5H15v-5.833a1.667 1.667 0 1 0-3.333 0V17.5H8.334v-5.833a5 5 0 0 1 5-5ZM5 7.5H1.667v10H5v-10ZM3.333 5a1.667 1.667 0 1 0 0-3.333 1.667 1.667 0 0 0 0 3.333Z" />
                        </svg>
                    </a>
                </div>
            </div>


            <img class="image" alt="Image" src="https://c.animaapp.com/ujIwT5MJ/img/image-21.png" />
        </div>
    </div>
</template>

<script>
export default {
    name: "HeroSection",
};
</script>

<style>
.section-subsection {
    align-self: stretch;

    background-color: rgba(255, 255, 255, 0.1);
    /* transparent background only */
    background: linear-gradient(180deg, rgba(44, 62, 80, 1) 0%, rgba(52, 73, 94, 1) 50%, rgba(61, 90, 107, 1) 100%);
    overflow: hidden;
    position: relative;
    width: 100%;
}

.section-subsection .socials {
    height: 48px;
    width: 48px;
    background-color: rgba(255, 255, 255, 0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 100%;
    margin-right: 12px;
}

.socials:hover {
    background-color: rgba(255, 255, 255, 0.3);
}

.section-subsection .rectangle {
    height: 140%;
    left: 100%;
    position: absolute;
    top: 0;
    width: 100%;
    max-width: 100%;
    transform: translateX(-50%) rotate(15deg);
    /* Rotate 15 degrees */
    background-color: #f5f3f0;
}

.section-subsection .div {
    display: flex;
    gap: 477px;
    height: 822px;
    left: 0;
    opacity: 0.1;
    position: absolute;
    top: 0;
    width: 100%;
}

.section-subsection .container-2 {
    background-color: #a67c5d;
    border-radius: 16777200px;
    filter: blur(64px);
    height: 288px;
    margin-left: 40px;
    margin-top: 80px;
    width: 288px;
}

.section-subsection .container-3 {
    background-color: #8b7968;
    border-radius: 16777200px;
    filter: blur(64px);
    height: 384px;
    margin-top: 358.5px;
    width: 384px;
}

.section-subsection .container-4 {
    display: flex;
    gap: 89.1px;
    height: 822px;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
    padding-right: 24px;
    box-sizing: border-box;
}

.section-subsection .container-5 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 24px;
    height: 320px;
    margin-left: 64px;
    margin-top: 251.2px;
    position: relative;
    width: 566.5px;
}

.section-subsection .container-6 {
    align-items: flex-start;
    align-self: stretch;
    display: flex;
    flex-direction: column;
    gap: 8px;
    height: 104px;
    position: relative;
    width: 100%;
}

.section-subsection .paragraph {
    align-self: stretch;
    height: 24px;
    position: relative;
    width: 100%;
}

.section-subsection .hello-i-m {
    color: #c9c4ba;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    left: 0;
    letter-spacing: -0.31px;
    line-height: 24px;
    position: absolute;
    top: 0;
    white-space: nowrap;
}

.section-subsection .heading {
    align-self: stretch;
    height: 72px;
    position: relative;
    width: 100%;
}

.section-subsection .text-wrapper {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 72px;
    font-weight: 500;
    left: 0;
    letter-spacing: 0.12px;
    line-height: 72px;
    position: absolute;
    top: 2px;
    white-space: nowrap;
}

.section-subsection .div-wrapper {
    align-self: stretch;
    height: 28px;
    position: relative;
    width: 100%;
}

.section-subsection .p {
    color: #b8b8b8;
    font-family: "Inter", Helvetica;
    font-size: 20px;
    font-weight: 400;
    left: 0;
    letter-spacing: -0.45px;
    line-height: 28px;
    position: absolute;
    top: 0;
    white-space: nowrap;
}

.section-subsection .creating-beautiful-wrapper {
    align-self: stretch;
    height: 52px;
    position: relative;
    width: 100%;
}

.section-subsection .creating-beautiful {
    color: #d4d1cc;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    left: 0;
    letter-spacing: -0.31px;
    line-height: 26px;
    position: absolute;
    top: 0;
    width: 546px;
}

.section-subsection .img {
    align-self: stretch;
    height: 64px;
    position: relative;
    width: 100%;
}

.section-subsection .image {
    aspect-ratio: 0.63;
    height: 675.36px;
    margin-top: 170px;
    margin-left: 150px;
    object-fit: cover;
    width: 476.72px;
    max-width: 100%;
    flex-shrink: 1;
}

/* Responsive design improvements */
@media (max-width: 1200px) {
    .section-subsection .container-4 {
        gap: 40px;
    }

    .section-subsection .container-5 {
        width: 50%;
        min-width: 400px;
    }
}

@media (max-width: 768px) {
    .section-subsection {
        height: auto;
        min-height: 600px;
    }

    .section-subsection .container-4 {
        flex-direction: column;
        height: auto;
        gap: 24px;
        padding: 24px;
    }

    .section-subsection .container-5 {
        width: 100%;
        margin-left: 0;
        margin-top: 0;
        min-width: auto;
    }

    .section-subsection .image {
        width: 100%;
        max-width: 300px;
        height: auto;
        margin-top: 0;
        align-self: center;
    }

    .section-subsection .text-wrapper {
        font-size: 48px;
        line-height: 48px;
    }
}
</style>
