<template>
    <div id="portfolio" class="div-wrapper-subsection">
        <div class="heading-7">
            <div class="text-wrapper-24">PORTFOLIO</div>
        </div>

        <div class="filterbar">
            <div class="filterbar-tabs" ref="filterTabs">
                <button v-for="filter in filters" :key="filter.value" type="button"
                    :class="['filter-tab', { active: activeFilter === filter.value }]" @click="setFilter(filter.value)">
                    {{ filter.label }}
                </button>
                <span class="filter-indicator" :style="indicatorStyle"></span>
            </div>
        </div>

        <div class="container-29">
            <div class="container-wrapper" v-show="filterMatches('design')">
                <div class="container-30">
                    <div class="container-31">
                        <div class="paragraph-4">
                            <div class="text-wrapper-29">designed</div>
                        </div>
                        <div class="heading-8">
                            <div class="text-wrapper-30">Project 1</div>
                        </div>
                        <div class="paragraph-4">
                            <div class="text-wrapper-31">E-commerce website</div>
                        </div>
                        <div class="container-32">
                            <button class="button">
                                <a href="https://www.figma.com/design/ypfnVpeysR40q6X7KMyWaz/E-Commerce?m=auto&t=djlbs7WhKfM4OmdK-6"
                                    target="_blank" rel="noopener noreferrer"
                                    class="text-wrapper-32 no-underline">DESIGN</a>
                            </button>
                            <button class="button" @click="openModal('project1')">
                                <div class="text-wrapper-32">MORE</div>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="container-33" v-show="filterMatches('design')">
                <div class="container-34">
                    <div class="container-31">
                        <div class="paragraph-4">
                            <div class="text-wrapper-29">coded, designed</div>
                        </div>
                        <div class="heading-8">
                            <div class="text-wrapper-30">Project 2</div>
                        </div>
                        <div class="paragraph-4">
                            <div class="text-wrapper-31">Task Management System</div>
                        </div>
                        <div class="container-32">
                            <button class="button" @click="openModal('project2a')">
                                <div class="text-wrapper-32">DEMO</div>
                            </button>
                            <button class="button" @click="openModal('project2b')">
                                <div class="text-wrapper-32">MORE</div>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="container-35" v-show="filterMatches('software')">
                <div class="container-34">
                    <div class="container-31">
                        <div class="paragraph-4">
                            <div class="text-wrapper-29">coded, designed</div>
                        </div>
                        <div class="heading-8">
                            <div class="text-wrapper-30">Project 3</div>
                        </div>
                        <div class="paragraph-4">
                            <div class="text-wrapper-31">Payroll System</div>
                        </div>
                        <div class="container-32">
                            <!--- <button class="button" @click="openModal('project3')">
                                <div class=" text-wrapper-32">DEMO
                                </div>
                            </button> --->
                            <button class="button" @click="openModal('project3')">
                                <div class="text-wrapper-32">MORE</div>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="container-36" v-show="filterMatches('analysis')">
                <div class="container-30">
                    <div class="container-31">
                        <div class="paragraph-4">
                            <div class="text-wrapper-29">coded</div>
                        </div>
                        <div class="heading-8">
                            <div class="text-wrapper-30">Project 4</div>
                        </div>
                        <div class="paragraph-4">
                            <div class="text-wrapper-31">Data-Driven Market Analysis
                            </div>
                        </div>
                        <div class="container-32">
                            <button class="button">
                                <a href="https://www.datacamp.com/datalab/w/3f1b5e08-811e-4a78-88dc-e0aab8604b6f/edit"
                                    target="_blank" rel="noopener noreferrer" class="text-wrapper-32">DEMO</a>
                            </button>
                            <button class="button" @click="openModal('project4')">
                                <div class="text-wrapper-32">MORE</div>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div v-if="isModalOpen && modalContent" class="portfolio-modal-overlay" @click.self="closeModal">
            <div class="portfolio-modal">
                <button class="modal-close-button" @click="closeModal" aria-label="Close project details">
                    &times;
                </button>
                <h3 class="modal-title">{{ modalContent.title }}</h3>
                <div v-if="modalContent.type === 'text'">
                    <p v-if="typeof modalContent.description === 'string'" class="modal-description">
                        {{ modalContent.description }}
                    </p>
                    <ul v-else-if="Array.isArray(modalContent.description)" class="modal-description-list">
                        <li v-for="(item, index) in modalContent.description" :key="index">{{ item }}</li>
                    </ul>
                </div>
                <div v-else-if="modalContent.type === 'video'" class="modal-video-wrapper">
                    <template v-if="modalContent.videoPlayer === 'file'">
                        <video :src="modalContent.videoSrc" autoplay controls playsinline muted preload="auto">
                            Sorry, your browser doesn't support embedded videos.
                        </video>
                    </template>
                    <iframe v-else :src="modalContent.videoUrl" title="Project video demo" frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen></iframe>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import ideaManagementDemo from "@/assets/videos/ims_video.mp4";

export default {
    name: "PortfolioSection",
    data() {
        return {
            activeFilter: "all",
            filters: [
                { label: "ALL", value: "all" },
                { label: "DESIGN", value: "design" },
                { label: "ANALYSIS", value: "analysis" },
                { label: "SOFTWARE", value: "software" },
            ],
            indicator: {
                width: 0,
                left: 0,
            },
            isModalOpen: false,
            modalContent: null,
            modalDetails: {
                project1: {
                    type: "text",
                    title: "E-commerce Website Demo",
                    description:
                        "An e-commerce website designed to showcase mobile phone products and services, with a focus on user experience and conversion optimization.",
                },
                project2a: {
                    type: "video",
                    title: "Idea Management System",
                    videoPlayer: "file",
                    videoSrc: ideaManagementDemo,
                },
                project2b: {
                    type: "text",
                    title: "Idea Management System",
                    description: [
                        "Collaborated with fellow students on group coursework to build a web enabled, role-based system for collecting ideas for improvement from staff in a large University.",
                        "Developed the website's user interface with JavaScript and CSS.",
                        "Implemented charts feature using Google Charts API."
                    ]
                },
                project3: {
                    type: "text",
                    title: "Payroll System Demo",
                    description: [
                        "A payroll system designed to be sold for commercial use with the target market being small to medium sized Zambian businesses. The payroll system is designed to be easy to navigate and perform efficient payroll related tasks and calculations. ",
                    ]
                },
                project4: {
                    type: "text",
                    title: "Market Analysis with Python",
                    description:
                        "A market analysis in Python to gauge demand and identify potential areas for growth of digital fitness products and services.",
                },
            },
        };
    },
    computed: {
        indicatorStyle() {
            return {
                width: this.indicator.width ? `${this.indicator.width}px` : "0px",
                transform: `translateX(${this.indicator.left}px)`,
            };
        },
    },
    mounted() {
        this.$nextTick(this.updateIndicator);
        window.addEventListener("resize", this.updateIndicator);
    },
    beforeDestroy() {
        window.removeEventListener("resize", this.updateIndicator);
    },
    beforeUnmount() {
        window.removeEventListener("resize", this.updateIndicator);
    },
    methods: {
        openModal(projectKey) {
            this.modalContent = this.modalDetails[projectKey] || null;
            this.isModalOpen = Boolean(this.modalContent);
        },
        closeModal() {
            this.isModalOpen = false;
            this.modalContent = null;
        },
        setFilter(filterValue) {
            if (this.activeFilter === filterValue) {
                return;
            }
            this.activeFilter = filterValue;
            this.$nextTick(this.updateIndicator);
        },
        filterMatches(category) {
            return this.activeFilter === "all" || this.activeFilter === category;
        },
        updateIndicator() {
            const container = this.$refs.filterTabs;
            if (!container) {
                return;
            }
            const activeTab = container.querySelector(".filter-tab.active");
            if (!activeTab) {
                return;
            }

            const containerRect = container.getBoundingClientRect();
            const tabRect = activeTab.getBoundingClientRect();
            this.indicator = {
                width: tabRect.width,
                left: tabRect.left - containerRect.left,
            };
        },
    },
};
</script>

<style>
.div-wrapper-subsection {
    align-items: center;
    align-self: stretch;
    background-color: #2c3e50;
    display: flex;
    flex: 0 0 auto;
    flex-direction: column;
    gap: 64px;
    padding: 96px 24px;
    position: relative;
    width: 100%;
    height: 1000px;
}

.div-wrapper-subsection .heading-7 {
    border-bottom-style: solid;
    border-bottom-width: 4px;
    border-color: #a67c5d;
    height: 60px;
    position: relative;
    width: 254.16px;
}

.div-wrapper-subsection .text-wrapper-24 {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 48px;
    font-weight: 400;
    left: -9px;
    letter-spacing: 0.35px;
    line-height: 48px;
    position: absolute;
    text-align: center;
    top: 1px;
    white-space: nowrap;
}

.div-wrapper-subsection .filterbar {
    width: 100%;
    max-width: 720px;
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.div-wrapper-subsection .filterbar-tabs {
    display: flex;
    justify-content: space-between;
    position: relative;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
}

.div-wrapper-subsection .filter-tab {
    flex: 1;
    background: transparent;
    border: none;
    color: #a2a3a5;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 0.5px;
    padding: 12px 8px;
    cursor: pointer;
    text-align: center;
    transition: color 0.2s ease;
}

.div-wrapper-subsection .filter-tab:hover {
    color: #ffffff;
}

.div-wrapper-subsection .filter-tab.active {
    color: #ffffff;
}

.div-wrapper-subsection .filter-indicator {
    position: absolute;
    bottom: -1px;
    left: 0;
    height: 2px;
    background: #ffffff;
    border-radius: 999px;
    transition: transform 0.3s ease, width 0.3s ease;
    will-change: transform, width;
}

.div-wrapper-subsection .container-29 {
    display: grid;
    gap: 32px;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 332px;
    width: 100%;
    max-width: 1200px;
    left: 50%;
    transform: translateX(-50%);
    padding: 0 24px;
}

.div-wrapper-subsection .container-wrapper {
    align-items: flex-start;
    background-image: url('@/assets/images/ecom.png');
    background-position: 50% 50%;
    background-size: cover;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
    grid-column: 1 / 2;
    grid-row: 1 / 2;
    height: 209.44px;
    overflow: hidden;
    position: relative;
    width: 100%;
    max-width: 372.33px;
    justify-self: center;
}

.div-wrapper-subsection .container-30 {
    align-items: center;
    align-self: stretch;
    background: linear-gradient(180deg,
            rgb(22, 29, 36) 0%,
            rgb(18, 25, 30) 100%), linear-gradient(0deg, rgba(0, 0, 0, 0.6) 0%, rgba(0, 0, 0, 0.6) 100%);
    display: flex;
    height: 209.43px;
    justify-content: center;
    opacity: 0;
    position: relative;
    width: 100%;
}

.div-wrapper-subsection .container-31 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 16px;
    height: 172px;
    position: relative;
    width: 266.78px;
}

.div-wrapper-subsection .paragraph-4 {
    align-self: stretch;
    height: 20px;
    position: relative;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.div-wrapper-subsection .text-wrapper-29 {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    width: 100%;
    letter-spacing: 1.25px;
    line-height: 20px;
    position: absolute;
    text-align: center;
    top: 1px;
    white-space: nowrap;
}

.div-wrapper-subsection .heading-8 {
    align-self: stretch;
    height: 32px;
    position: relative;
    width: 100%;
}

.div-wrapper-subsection .text-wrapper-30 {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 24px;
    font-weight: 400;
    width: 100%;
    letter-spacing: 1.27px;
    line-height: 32px;
    position: absolute;
    text-align: center;
    top: 0;
}

.div-wrapper-subsection .text-wrapper-31 {
    color: #c9c4ba;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    width: 100%;
    letter-spacing: -0.15px;
    line-height: 20px;
    position: absolute;
    text-align: center;
    top: 1px;
    white-space: nowrap;
}

.div-wrapper-subsection .container-32 {
    align-items: flex-start;
    align-self: stretch;
    display: flex;
    gap: 16px;
    height: 52px;
    justify-content: center;
    padding: 16px 0.01px 0px 0px;
    position: relative;
    width: 100%;
}

.div-wrapper-subsection .button {
    all: unset;
    cursor: pointer;
    background-color: #ffffff1a;
    border-radius: 16777200px;
    box-sizing: border-box;
    height: 36px;
    position: relative;
    width: 91.75px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.div-wrapper-subsection .button:hover {
    background-color: #ffffff33;
    transform: scale(1.05);
    transition: transform 0.2s ease;
}

.div-wrapper-subsection .text-wrapper-32 {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 14px;
    font-weight: 400;
    letter-spacing: 0.55px;
    line-height: 20px;
    position: absolute;
    white-space: nowrap;
}

.div-wrapper-subsection .button-2 {
    all: unset;
    background-color: #ffffff1a;
    border-radius: 16777200px;
    box-sizing: border-box;
    height: 36px;
    position: relative;
    width: 90.73px;
}

.div-wrapper-subsection .container-33 {
    align-items: flex-start;
    background-image: url('@/assets/images/ims.png');

    background-position: 50% 50%;
    background-size: cover;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
    grid-column: 2 / 3;
    grid-row: 1 / 2;
    height: 209.44px;
    overflow: hidden;
    position: relative;
    width: 100%;
    max-width: 372.34px;
    justify-self: center;
}

.div-wrapper-subsection .container-34 {
    align-items: center;
    align-self: stretch;
    background: linear-gradient(180deg,
            rgb(22, 29, 36) 0%,
            rgb(18, 25, 30) 100%), linear-gradient(0deg, rgba(0, 0, 0, 0.6) 0%, rgba(0, 0, 0, 0.6) 100%);
    display: flex;
    height: 209.44px;
    justify-content: center;
    opacity: 0;
    padding: 0px 0.01px 0px 0px;
    position: relative;
    width: 100%;
}

.div-wrapper-subsection .container-35 {
    align-items: flex-start;
    background-image: url('@/assets/images/payroll.png');
    background-position: 50% 50%;
    background-size: cover;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
    grid-column: 1 / 2;
    grid-row: 2 / 3;
    height: 209.44px;
    overflow: hidden;
    position: relative;
    width: 100%;
    max-width: 372.34px;
    justify-self: center;
}

.div-wrapper-subsection .container-36 {
    align-items: flex-start;
    background-image: url('@/assets/images/products.png');
    background-position: 50% 50%;
    background-size: cover;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
    grid-column: 2 / 3;
    grid-row: 2 / 3;
    height: 209.44px;
    overflow: hidden;
    position: relative;
    width: 100%;
    max-width: 372.33px;
    justify-self: center;
}

.div-wrapper-subsection .paragraph-5 {
    height: 28px;
    width: 100%;
}

.div-wrapper-subsection .text-wrapper-34 {
    color: #c9c4ba;
    font-family: "Inter", Helvetica;
    font-size: 20px;
    font-weight: 400;
    letter-spacing: -0.45px;
    line-height: 28px;
}

.portfolio-modal-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.65);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1000;
    padding: 24px;
}

.portfolio-modal {
    background: #ffffff;
    border-radius: 16px;
    max-width: 640px;
    width: min(90vw, 640px);
    padding: 32px;
    position: relative;
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.25);
    color: #2c3e50;
}

.modal-close-button {
    position: absolute;
    top: 16px;
    right: 16px;
    border: none;
    background: transparent;
    font-size: 28px;
    cursor: pointer;
    color: #2c3e50;
}

.modal-title {
    font-family: "Inter", Helvetica;
    font-size: 24px;
    margin-bottom: 16px;
}

.modal-description {
    font-family: "Inter", Helvetica;
    font-size: 16px;
    line-height: 1.6;
    white-space: pre-line;
}

.modal-description-list {
    font-family: "Inter", Helvetica;
    font-size: 16px;
    line-height: 1.6;
    margin: 0;
    padding-left: 24px;
    list-style-type: disc;
}

.modal-description-list li {
    margin-bottom: 8px;
}

.modal-description-list li:last-child {
    margin-bottom: 0;
}

.modal-video-wrapper {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    border-radius: 12px;
    box-shadow: inset 0 0 0 1px rgba(44, 62, 80, 0.08);
}

.modal-video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
}

.modal-video-wrapper video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
    border-radius: 12px;
    background: #000;
    object-fit: cover;
}


/* Make overlays hidden by default */
.div-wrapper-subsection .container-30,
.div-wrapper-subsection .container-34 {
    opacity: 0;
    transition: opacity 0.4s ease;
    /* smooth fade */
    pointer-events: none;
    /* avoid blocking clicks when hidden */
}

/* When you hover over the card wrapper (the background container) */
.div-wrapper-subsection .container-wrapper:hover .container-30,
.div-wrapper-subsection .container-33:hover .container-34,
.div-wrapper-subsection .container-35:hover .container-34,
.div-wrapper-subsection .container-36:hover .container-30 {
    opacity: 1;
    pointer-events: auto;
}


/* Optional – add a subtle zoom effect on the image */
.div-wrapper-subsection .container-wrapper,
.div-wrapper-subsection .container-33,
.div-wrapper-subsection .container-35,
.div-wrapper-subsection .container-36 {
    transition: transform 0.4s ease;
}

.div-wrapper-subsection .container-wrapper:hover,
.div-wrapper-subsection .container-33:hover,
.div-wrapper-subsection .container-35:hover,
.div-wrapper-subsection .container-36:hover {
    transform: scale(1.02);
}
</style>
