<template>
    <div class="section-wrapper-subsection">
        <div class="heading-2">
            <div class="text-wrapper-2">ABOUT ME</div>
        </div>

        <div class="my-name-is-tomasz-wrapper">
            <p class="my-name-is-tomasz">
                My name is Chikondi Banda, I&#39;m a MSc Data, Inequality and Society
                student at the University of Edinburgh in Scotland and I have been
                developing software for over 2 years.
            </p>
        </div>

        <div class="container-7" />

        <div class="container-8">
            <div class="skill-card hover:drop-shadow-lg">
                <div class="icon-jam-icons-instance-wrapper">
                    <IconJamIcons class="icon-jam-icons-outline-logos-pencil" />
                </div>

                <div class="heading-3">
                    <div class="text-wrapper-3">DESIGN</div>
                </div>

                <div class="i-can-design-the-wrapper">
                    <p class="i-can-design-the">
                        My professional work experience is largely in UI/UX design. I have
                        an exceptional ability to design functional software
                    </p>
                </div>
            </div>

            <div class="container-10 hover:drop-shadow-lg">
                <div class="icon-jam-icons-instance-wrapper">
                    <IconJamIconsWrapper class="icon-jam-icons-outline-logos-computer-alt" />
                </div>

                <div class="heading-4">
                    <div class="text-wrapper-4">DEVELOPMENT</div>
                </div>

                <div class="paragraph-2">
                    <p class="based-on-a-project">
                        With experience in both frontend and backend development, I am
                        able to deliver full-stack applications.
                    </p>
                </div>
            </div>

            <div class="container-11 hover:drop-shadow-lg">
                <div class="icon-heroicons-wrapper">
                    <IconHeroicons class="icon-heroicons-outline-search" />
                </div>

                <div class="heading-4">
                    <div class="text-wrapper-5">ANALYSIS</div>
                </div>

                <div class="paragraph-2">
                    <p class="in-case-of-any">
                        My Masters degree program and personal projects have developed my
                        quantitative analysis skills.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import IconHeroicons from "../components/icons/IconHeroicons.vue";
import IconJamIcons from "../components/icons/IconJamIcons.vue";
import IconJamIconsWrapper from "../components/icons/IconJamIconsWrapper.vue";

export default {
    name: "SectionWrapperSubsection",
    components: {
        IconHeroicons,
        IconJamIcons,
        IconJamIconsWrapper,
    },
};
</script>

<style>
.section-wrapper-subsection {
    align-items: center;
    align-self: stretch;
    background-color: #ffffff;
    display: flex;
    flex: 0 0 auto;
    flex-direction: column;
    gap: 48px;
    padding: 96px 167px;
    position: relative;
    width: 100%;
}

.section-wrapper-subsection .heading-2 {
    border-bottom-style: solid;
    border-bottom-width: 4px;
    border-color: #a67c5d;
    height: 60px;
    position: relative;
    width: 234.98px;
}

.section-wrapper-subsection .text-wrapper-2 {
    color: #2c3e50;
    font-family: "Inter", Helvetica;
    font-size: 48px;
    font-weight: 400;
    left: -10px;
    letter-spacing: 0.35px;
    line-height: 48px;
    position: absolute;
    text-align: center;
    top: 1px;
    white-space: nowrap;
}

.section-wrapper-subsection .my-name-is-tomasz-wrapper {
    height: 87.75px;
    margin-left: -0.50px;
    margin-right: -0.50px;
    position: relative;
    width: 896px;
}

.section-wrapper-subsection .my-name-is-tomasz {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 18px;
    font-weight: 400;
    left: 1px;
    letter-spacing: -0.44px;
    line-height: 29.2px;
    position: absolute;
    text-align: center;
    top: 1px;
    width: 894px;
}

.section-wrapper-subsection .container-7 {
    background: linear-gradient(180deg,
            rgba(0, 0, 0, 0) 0%,
            rgba(166, 124, 93, 1) 50%,
            rgba(0, 0, 0, 0) 100%);
    height: 1px;
    margin-left: -0.50px;
    margin-right: -0.50px;
    position: relative;
    width: 896px;
}

.section-wrapper-subsection .container-8 {
    height: 341.75px;
    margin-left: -0.50px;
    margin-right: -0.50px;
    position: relative;
    width: 896px;
}

.section-wrapper-subsection .skill-card {
    background: linear-gradient(180deg,
            rgba(245, 243, 240, 1) 0%,
            rgba(255, 255, 255, 1) 100%);
    border-radius: 16px;
    box-shadow: 0px 1px 2px -1px #0000001a, 0px 1px 3px #0000001a;
    display: flex;
    flex-direction: column;
    height: 310px;
    left: 0;
    position: absolute;
    top: 32px;
    width: 277px;
    transition: all 0.3s ease;
}

.section-wrapper-subsection .skill-card:hover {
    box-shadow: 0px 10px 25px -5px rgba(0, 0, 0, 0.1), 0px 10px 10px -5px rgba(0, 0, 0, 0.04);
    transform: translateY(-2px);
}

.section-wrapper-subsection .icon-jam-icons-instance-wrapper {
    background: linear-gradient(180deg,
            rgba(166, 124, 93, 1) 0%,
            rgba(139, 121, 104, 1) 100%);
    border-radius: 100%;
    display: flex;
    height: 64px;
    margin-left: 106.7px;
    margin-top: 32px;
    opacity: 0.2;
    width: 64px;
}

.section-wrapper-subsection .icon-jam-icons-outline-logos-pencil {
    left: unset !important;
    margin-left: 19.8px !important;
    margin-top: 19.8px !important;
    position: unset !important;
    top: unset !important;
}

.section-wrapper-subsection .heading-3 {
    display: flex;
    margin-left: 32px;
    margin-top: 24px;
    width: 213.33px;
}

.section-wrapper-subsection .text-wrapper-3 {
    color: #21293d;
    font-family: "Inter", Helvetica;
    font-size: 20px;
    font-weight: 400;
    height: 28px;
    letter-spacing: 0.05px;
    line-height: 28px;
    margin-left: 70.0px;
    text-align: center;
    white-space: nowrap;
    width: 75px;
}

.section-wrapper-subsection .i-can-design-the-wrapper {
    display: flex;
    height: 113.75px;
    margin-left: 32px;
    margin-top: 16px;
    width: 213.33px;
}

.section-wrapper-subsection .i-can-design-the {
    color: #5a5a5a;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    height: 91px;
    letter-spacing: -0.15px;
    line-height: 22.8px;
    margin-left: 0.1px;
    margin-top: 1px;
    text-align: center;
    width: 214px;
}

.section-wrapper-subsection .container-10 {
    background: linear-gradient(180deg,
            rgba(245, 243, 240, 1) 0%,
            rgba(255, 255, 255, 1) 100%);
    border-radius: 16px;
    box-shadow: 0px 1px 2px -1px #0000001a, 0px 1px 3px #0000001a;
    display: flex;
    flex-direction: column;
    height: 310px;
    left: 309px;
    position: absolute;
    top: 32px;
    width: 277px;
    transition: all 0.3s ease;
}

.section-wrapper-subsection .container-10:hover {
    box-shadow: 0px 10px 25px -5px rgba(0, 0, 0, 0.1), 0px 10px 10px -5px rgba(0, 0, 0, 0.04);
    transform: translateY(-2px);
}

.section-wrapper-subsection .icon-jam-icons-outline-logos-computer-alt {
    left: unset !important;
    margin-left: 19.5px !important;
    margin-top: 19.8px !important;
    position: unset !important;
    top: unset !important;
}

.section-wrapper-subsection .heading-4 {
    display: flex;
    margin-left: 32px;
    margin-top: 24px;
    width: 213.34px;
}

.section-wrapper-subsection .text-wrapper-4 {
    color: #21293d;
    font-family: "Inter", Helvetica;
    font-size: 20px;
    font-weight: 400;
    height: 28px;
    letter-spacing: 0.05px;
    line-height: 28px;
    margin-left: 32.7px;
    text-align: center;
    white-space: nowrap;
    width: 149px;
}

.section-wrapper-subsection .paragraph-2 {
    display: flex;
    margin-left: 32px;
    margin-top: 16px;
    width: 213.34px;
}

.section-wrapper-subsection .based-on-a-project {
    color: #5a5a5a;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    height: 91px;
    letter-spacing: -0.15px;
    line-height: 22.8px;
    margin-left: 0.7px;
    margin-top: 1px;
    text-align: center;
    width: 212px;
}

.section-wrapper-subsection .container-11 {
    background: linear-gradient(180deg,
            rgba(245, 243, 240, 1) 0%,
            rgba(255, 255, 255, 1) 100%);
    border-radius: 16px;
    box-shadow: 0px 1px 2px -1px #0000001a, 0px 1px 3px #0000001a;
    display: flex;
    flex-direction: column;
    height: 310px;
    left: 619px;
    position: absolute;
    top: 32px;
    width: 277px;
    transition: all 0.3s ease;
}

.section-wrapper-subsection .container-11:hover {
    box-shadow: 0px 10px 25px -5px rgba(0, 0, 0, 0.1), 0px 10px 10px -5px rgba(0, 0, 0, 0.04);
    transform: translateY(-2px);
}

.section-wrapper-subsection .icon-heroicons-wrapper {
    background: linear-gradient(180deg,
            rgba(166, 124, 93, 1) 0%,
            rgba(139, 121, 104, 1) 100%);
    border-radius: 16777200px;
    height: 64px;
    margin-left: 106.7px;
    margin-top: 32px;
    opacity: 0.2;
    position: relative;
    width: 64px;
}

.section-wrapper-subsection .icon-heroicons-outline-search {
    height: 37.50% !important;
    left: 31.52% !important;
    top: 30.86% !important;
    width: 37.50% !important;
}

.section-wrapper-subsection .text-wrapper-5 {
    color: #21293d;
    font-family: "Inter", Helvetica;
    font-size: 20px;
    font-weight: 400;
    height: 28px;
    letter-spacing: 0.05px;
    line-height: 28px;
    margin-left: 57.9px;
    text-align: center;
    white-space: nowrap;
    width: 98px;
}

.section-wrapper-subsection .in-case-of-any {
    color: #5a5a5a;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    height: 91px;
    letter-spacing: -0.15px;
    line-height: 22.8px;
    margin-left: 9.2px;
    margin-top: 1px;
    text-align: center;
    width: 195px;
}
</style>
