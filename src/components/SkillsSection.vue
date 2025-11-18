<template>
    <div id="skills" class="container-wrapper-subsection">
        <div class="container-12">
            <div class="heading-5">
                <div class="text-wrapper-6">SKILLS</div>
            </div>

            <div class="container-13">
                <div class="container-14">
                    <div class="heading-6">
                        <div class="text-wrapper-7">USING NOW:</div>
                    </div>

                    <div class="container-15">
                        <div class="container-16">
                            <div class="container-17">
                                <img src="@/assets/images/python.png" alt="Python" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">PYTHON</div>
                            </div>
                        </div>

                        <div class="container-18">
                            <div class="container-17">
                                <img src="@/assets/images/vue.png" alt="Vue.js" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">VUE.JS</div>
                            </div>
                        </div>

                        <div class="container-19">
                            <div class="container-17">
                                <img src="@/assets/images/tailwind.png" alt="Tailwind CSS" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">TAILWIND CSS</div>
                            </div>
                        </div>

                        <div class="container-20">
                            <div class="container-17">
                                <img src="@/assets/images/java.png" alt="Java" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">JAVA</div>
                            </div>
                        </div>

                        <div class="container-21">
                            <div class="container-17">
                                <img src="@/assets/images/postgresql.png" alt="PostgreSQL" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">POSTGRESQL</div>
                            </div>
                        </div>

                        <div class="container-22">
                            <div class="container-17">
                                <img src="@/assets/images/tb.png" alt="Tableau" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">TABLEAU</div>
                            </div>
                        </div>

                        <div class="container-23">
                            <div class="container-17">
                                <img src="@/assets/images/Typescript.png" alt="TypeScript" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">TYPESCRIPT</div>
                            </div>
                        </div>

                        <div class="container-24">
                            <div class="container-17">
                                <img src="@/assets/images/figma.png" alt="Figma" class="skill-image" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">FIGMA</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="container-25">
                    <div class="heading-6">
                        <div class="text-wrapper-7">LEARNING:</div>
                    </div>

                    <div class="container-26">
                        <div class="container-16">
                            <div class="container-27" />
                            <div class="container-17">
                                <img src="@/assets/images/mongodb.png" alt="Figma" class="skill-image" />
                            </div>
                            <div class="paragraph-3">
                                <div class="text-wrapper-8">MONGODB</div>
                            </div>
                        </div>

                        <div class="container-18">
                            <div class="container-27">
                                <Icon icon="ph:monitor-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">LLMs</div>
                            </div>
                        </div>

                        <div class="container-24">
                            <div class="container-27">
                                <Icon icon="mdi-light:pencil" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">WRITING</div>
                            </div>
                        </div>

                        <div class="container-19">
                            <div class="container-27">
                                <Icon icon="ph:speaker-high-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">PRESENTATIONS</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="container-25">
                    <div class="heading-6">
                        <div class="text-wrapper-7">OTHER SKILLS:</div>
                    </div>

                    <div class="container-26">
                        <div class="container-16">
                            <div class="container-28">
                                <Icon icon="ph:chat-circle-dots-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">ENGLISH C2</div>
                            </div>
                        </div>

                        <div class="container-18">
                            <div class="container-28">
                                <Icon icon="ph:paint-brush-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">GRAPHIC DESIGN</div>
                            </div>
                        </div>

                        <div class="container-24">
                            <div class="container-28">
                                <Icon icon="ph:camera-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">PHOTOGRAPHY</div>
                            </div>
                        </div>

                        <div class="container-19">
                            <div class="container-28">
                                <Icon icon="ph:device-mobile-camera-light" class="w-full h-full" color="#3d5a6b" />
                            </div>

                            <div class="paragraph-3">
                                <div class="text-wrapper-8">ANDROID DEVELOPMENT</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { Icon } from "@iconify/vue";
export default {
    name: "SkillsSection",
    components: {
        Icon,
    },
};
</script>

<style>
.container-wrapper-subsection {
    align-items: flex-start;
    align-self: stretch;
    background: linear-gradient(180deg,
            rgba(245, 243, 240, 1) 0%,
            rgba(232, 229, 224, 1) 100%);
    display: flex;
    flex-direction: column;
    height: 1132px;
    padding: 96px 102.5px 0px;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-12 {
    display: flex;
    justify-content: center;
    height: 940px;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .heading-5 {
    border-bottom-style: solid;
    border-bottom-width: 4px;
    border-color: #a67c5d;
    display: flex;
    height: 60px;
    position: absolute;
    top: 0;
    width: 149px;
}

.container-wrapper-subsection .text-wrapper-6 {
    color: #2c3e50;
    font-family: "Inter", Helvetica;
    font-size: 48px;
    font-weight: 400;
    height: 48px;
    letter-spacing: 0.35px;
    line-height: 48px;
    margin-left: -5px;
    margin-top: 0.5px;
    text-align: center;
    white-space: nowrap;
    width: 161px;
}

.container-wrapper-subsection .container-13 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 64px;
    height: 816px;
    left: 0;
    position: absolute;
    top: 124px;
    width: 100%;
}

.container-wrapper-subsection .container-14 {
    align-items: flex-start;
    align-self: stretch;
    display: flex;
    flex-direction: column;
    gap: 32px;
    height: 328px;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .heading-6 {
    align-self: stretch;
    height: 32px;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .text-wrapper-7 {
    color: #2c3e50;
    font-family: "Inter", Helvetica;
    font-size: 24px;
    font-weight: 400;
    left: 0;
    letter-spacing: 0.67px;
    line-height: 32px;
    position: absolute;
    top: 0;
    white-space: nowrap;
}

.container-wrapper-subsection .container-15 {
    display: grid;
    gap: 32px;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    grid-template-rows: repeat(2, minmax(0, 1fr));
    height: 264px;
    left: 0;
    position: absolute;
    top: 64px;
    width: 100%;
}

.container-wrapper-subsection .container-16 {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-17 {
    border-radius: 16px;
    height: 80px;
    left: 76px;
    position: absolute;
    top: 0;
    width: 80px;
}

.container-wrapper-subsection .paragraph-3 {
    display: flex;
    height: 24px;
    left: 0;
    position: absolute;
    top: 92px;
    width: 232px;
}

.container-wrapper-subsection .text-wrapper-8 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 100%;
}

.container-wrapper-subsection .container-18 {
    grid-column: 2 / 3;
    grid-row: 1 / 2;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .text-wrapper-9 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 57.1px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 118px;
}

.container-wrapper-subsection .container-19 {
    grid-column: 4 / 5;
    grid-row: 1 / 2;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-20 {
    grid-column: 1 / 2;
    grid-row: 2 / 3;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-21 {
    grid-column: 2 / 3;
    grid-row: 2 / 3;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-22 {
    grid-column: 3 / 4;
    grid-row: 2 / 3;
    height: 100%;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-23 {
    grid-column: 4 / 5;
    grid-row: 2 / 3;
    height: 100%;
    position: relative;
    width: 100%;
}


.container-wrapper-subsection .container-24 {
    grid-column: 3 / 4;
    grid-row: 1 / 2;
    height: 100%;
    position: relative;
    width: 100%;
}


.container-wrapper-subsection .container-25 {
    align-items: flex-start;
    align-self: stretch;
    display: flex;
    flex-direction: column;
    gap: 32px;
    height: 180px;
    position: relative;
    width: 100%;
}

.container-wrapper-subsection .container-26 {
    display: grid;
    gap: 32px;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    grid-template-rows: repeat(1, minmax(0, 1fr));
    height: 116px;
    left: 0;
    position: absolute;
    top: 64px;
    width: 100%;
}

.container-wrapper-subsection .container-27 {
    border-radius: 16px;
    height: 80px;
    left: 76px;
    position: absolute;
    top: 0;
    width: 80px;
}

.container-wrapper-subsection .container-28 {
    border-radius: 16px;
    height: 80px;
    left: 76px;
    position: absolute;
    top: 0;
    width: 80px;
}

.container-wrapper-subsection .text-wrapper-20 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 66.8px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 99px;
}

.container-wrapper-subsection .text-wrapper-21 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 54.8px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 123px;
}

.container-wrapper-subsection .text-wrapper-22 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 99.5px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 34px;
}

.container-wrapper-subsection .text-wrapper-23 {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 110.0px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 12px;
}

/* Skill image styling */
.container-wrapper-subsection .skill-image {
    width: 100%;
    height: 100%;
    object-fit: contain;
    border-radius: 16px;
}

/* Skill icon styling */
.container-wrapper-subsection .skill-icon {
    width: 50%;
    height: 50%;
    margin: 25%;
    fill: #3b82f6;
    filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.15));
}
</style>
