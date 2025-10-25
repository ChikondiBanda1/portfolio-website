<template>
  <div class="portfolio-website min-h-screen w-full">
    <div class="app w-full">
      <SectionSubsection />
      <SectionWrapperSubsection />
      <ContainerWrapperSubsection />
      <DivWrapperSubsection />
      <DivSubsection />
      <FooterSubsection />
    </div>

    <div class="app-2" :class="{ 'scrolled': isScrolled }">
      <div class="container-43">
        <div class="text">
          <div class="text-wrapper-41">CB</div>
        </div>
      </div>

      <div class="container-44">
        <button class="button-5">
          <div class="text-wrapper-42">About</div>
        </button>

        <button class="button-6">
          <div class="text-wrapper-42">Skills</div>
        </button>

        <button class="button-7">
          <div class="text-wrapper-42">Portfolio</div>
        </button>

        <button class="button-8">
          <div class="text-wrapper-43">Contact Me</div>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import SectionSubsection from '../components/SectionSubsection.vue';
import SectionWrapperSubsection from '../components/SectionWrapperSubsection.vue';
import ContainerWrapperSubsection from '../components/ContainerWrapperSubsection.vue';
import DivWrapperSubsection from '../components/DivWrapperSubsection.vue';
import DivSubsection from '../components/DivSubsection.vue';
import FooterSubsection from '../components/FooterSubsection.vue';

export default {
  name: 'PortfolioWebsite',
  components: {
    SectionSubsection,
    SectionWrapperSubsection,
    ContainerWrapperSubsection,
    DivWrapperSubsection,
    DivSubsection,
    FooterSubsection,
  },
  data() {
    return {
      isScrolled: false
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50;
    }
  }
};
</script>

<style>
.portfolio-website {
  align-items: center;
  background-color: #ffffff;
  display: flex;
  flex-direction: column;
  gap: 10px;
  position: relative;
  width: 100%;
  min-height: 100vh;
}

.portfolio-website .app {
  align-items: flex-start;
  align-self: stretch;
  background-color: #f5f3f0;
  display: flex;
  flex-direction: column;
  position: relative;
  padding: 0px;
  margin: 0px;
  width: 100%;
  flex: 1;
}

.portfolio-website .app-2 {
  align-items: center;
  display: flex;
  height: 70px;
  justify-content: space-between;
  position: fixed;
  width: 100%;
  padding: 16px 48px;
  z-index: 1000;
  transition: background-color 0.3s ease;
}

.portfolio-website .app-2.scrolled {
  background-color: rgba(44, 62, 80, 0.8);
  backdrop-filter: blur(7px);
}

.portfolio-website .app-2.scrolled .text-wrapper-42 {
  color: #ffffff;
}

.portfolio-website .app-2.scrolled .text-wrapper-43 {
  color: #ffffff;
}

.portfolio-website .container-43 {
  align-items: center;
  background: linear-gradient(180deg,
      #a67c5d 0%,
      #8b7968 100%);
  border-radius: 16777200px;
  display: flex;
  height: 40px;
  justify-content: center;
  padding: 0px 0.01px 0px 0px;
  position: relative;
  width: 40px;
}

.portfolio-website .text {
  height: 24px;
  position: relative;
  width: 20.99px;
}

.portfolio-website .text-wrapper-41 {
  color: #ffffff;
  font-family: "Inter-Regular", Helvetica;
  font-size: 16px;
  font-weight: 400;
  left: 0;
  letter-spacing: -0.31px;
  line-height: 24px;
  position: absolute;
  top: 0;
  white-space: nowrap;
}

.portfolio-website .container-44 {
  align-items: center;
  display: flex;
  gap: 32px;
  height: 40px;
  position: relative;
  width: 370.36px;
}

.portfolio-website .button-5 {
  all: unset;
  box-sizing: border-box;
  height: 24px;
  position: relative;
  width: 43.65px;
}

.portfolio-website .text-wrapper-42 {
  color: #2c3e50;
  font-family: "Inter-Regular", Helvetica;
  font-size: 16px;
  font-weight: 400;
  left: 0;
  letter-spacing: -0.31px;
  line-height: 24px;
  position: absolute;
  top: 0;
  white-space: nowrap;
  transition: color 0.3s ease;
}

.portfolio-website .button-6 {
  all: unset;
  box-sizing: border-box;
  height: 24px;
  position: relative;
  width: 37.43px;
}

.portfolio-website .button-7 {
  all: unset;
  box-sizing: border-box;
  height: 24px;
  position: relative;
  width: 60.98px;
}

.portfolio-website .button-8 {
  all: unset;
  background-color: #2c3e50;
  border-radius: 16777200px;
  box-sizing: border-box;
  flex: 1;
  flex-grow: 1;
  height: 40px;
  position: relative;
}

.portfolio-website .text-wrapper-43 {
  color: #ffffff;
  font-family: "Inter-Regular", Helvetica;
  font-size: 16px;
  font-weight: 400;
  left: 24px;
  letter-spacing: -0.31px;
  line-height: 24px;
  position: absolute;
  top: 8px;
  white-space: nowrap;
  transition: color 0.3s ease;
}

/* Responsive design improvements */
@media (max-width: 768px) {
  .portfolio-website .app-2 {
    left: 16px;
    width: calc(100% - 32px);
    flex-wrap: wrap;
    height: auto;
    gap: 16px;
  }

  .portfolio-website .container-44 {
    flex-wrap: wrap;
    gap: 16px;
    width: auto;
  }

  .portfolio-website .button-8 {
    width: 100%;
    max-width: 200px;
  }
}

@media (max-width: 480px) {
  .portfolio-website .app-2 {
    left: 12px;
    width: calc(100% - 24px);
    top: 12px;
  }

  .portfolio-website .container-44 {
    gap: 12px;
  }
}
</style>