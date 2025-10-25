<template>
    <div class="div-subsection">
        <div class="container-37">
            <div class="w-full flex justify-center">
                <div class="heading-9">
                    <div class="text-wrapper-35">CONTACT</div>
                </div>
            </div>


            <div class="feel-free-to-reach-wrapper">
                <p class="feel-free-to-reach">
                    Feel free to reach out if you want to collaborate on a project, have
                    a question, or just want to connect.
                </p>
            </div>

            <form class="form" @submit.prevent="handleSubmit">
                <div class="container-38">
                    <div class="label">
                        <div class="text-wrapper-36">ENTER YOUR NAME*</div>
                    </div>

                    <input type="text" v-model="formData.name" class="div-2" placeholder="Your Name" />
                </div>

                <div class="container-39">
                    <div class="label">
                        <div class="text-wrapper-36">ENTER YOUR EMAIL*</div>
                    </div>

                    <input type="email" v-model="formData.email" class="div-2" placeholder="you@example.com" />
                </div>

                <div class="container-39">
                    <div class="label">
                        <div class="text-wrapper-36">PHONE NUMBER</div>
                    </div>

                    <input type="tel" v-model="formData.phone" class="div-2" placeholder="123-456-7890" />
                </div>

                <div class="container-40">
                    <div class="label">
                        <div class="text-wrapper-36">YOUR MESSAGE*</div>
                    </div>

                    <textarea class="text-area" v-model="formData.message"
                        placeholder="Type your message here..."></textarea>
                </div>

                <div class="w-full flex justify-center">
                    <button class="button-3" type="submit">
                        <div class="text-wrapper-37">SUBMIT</div>
                    </button>
                </div>

            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: "DivSubsection",
    data() {
        return {
            formData: {
                name: "",
                email: "",
                phone: "",
                message: "",
            },
        };
    },
    methods: {
        handleSubmit() {
            // Log the form data
            console.log("Form submitted!", this.formData);

            // Show a normal JS notification
            alert("Your message has been sent!");

            // Reset form
            this.formData = { name: "", email: "", phone: "", message: "" };
        },
    },
};
</script>

<style>
.div-subsection {
    align-items: center;
    align-self: stretch;
    background: linear-gradient(180deg,
            rgba(245, 243, 240, 1) 0%,
            rgba(232, 229, 224, 1) 100%);
    display: flex;
    flex-direction: column;
    height: 1020px;
    padding: 96px 166.5px 0px;
    position: relative;
    width: 100%;
}

.div-subsection .container-37 {
    display: flex;
    align-items: center;
    height: 828px;
    position: relative;
    width: 100%;
}

.div-subsection .heading-9 {
    border-bottom-style: solid;
    border-bottom-width: 4px;
    border-color: #a67c5d;
    display: flex;
    height: 60px;
    position: absolute;
    top: 0;
    width: 216px;
}

.div-subsection .text-wrapper-35 {
    color: #2c3e50;
    font-family: "Inter", Helvetica;
    font-size: 48px;
    font-weight: 400;
    height: 48px;
    letter-spacing: 0.35px;
    line-height: 48px;
    margin-left: -8px;
    margin-top: 0.5px;
    text-align: center;
    white-space: nowrap;
    width: 233px;
}

.div-subsection .feel-free-to-reach-wrapper {
    display: flex;
    height: 26px;
    left: 24px;
    position: absolute;
    top: 124px;
    width: 100%;
    align-items: center;
}

.div-subsection .feel-free-to-reach {
    color: #3d5a6b;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 26px;
    letter-spacing: -0.31px;
    line-height: 26px;
    margin-left: 55.6px;
    margin-top: -0.5px;
    text-align: center;
    white-space: nowrap;
    width: 100%;
}

.div-subsection .form {
    display: flex;
    flex-direction: column;
    height: 630px;
    left: 24px;
    position: absolute;
    top: 198px;
    width: 100%;
}

.div-subsection .container-38 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 8px;
    height: 82px;
    position: relative;
    width: 100%;
}

.div-subsection .label {
    align-self: stretch;
    height: 24px;
    position: relative;
    width: 100%;
}

.div-subsection .text-wrapper-36 {
    color: #2c3e50;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    left: 0;
    letter-spacing: 0.49px;
    line-height: 24px;
    position: absolute;
    top: 0;
    white-space: nowrap;
}

.div-subsection .div-2 {
    align-self: stretch;
    border-bottom-style: solid;
    border-bottom-width: 2px;
    border-color: #a67c5d;
    height: 50px;
    position: relative;
    width: 100%;
    color: #2c3e50;
    padding-left: 8px;
}

.div-subsection .div-2,
.div-subsection .text-area {
    background-color: #ffffff;
    /* white background */
    border: none;
    /* remove any default border */
    outline: none;
    /* remove focus outline */
}

.div-subsection .container-39 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 8px;
    height: 82px;
    margin-top: 24px;
    position: relative;
    width: 100%;
}

.div-subsection .container-40 {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    gap: 8px;
    height: 208px;
    margin-top: 24px;
    position: relative;
    width: 100%;
}

.div-subsection .text-area {
    align-self: stretch;
    border-bottom-style: solid;
    border-bottom-width: 2px;
    border-color: #a67c5d;
    height: 170px;
    position: relative;
    width: 100%;
    color: #2c3e50;
    padding-left: 8px;
}

.div-subsection .button-3 {
    all: unset;
    background-color: #2c3e50;
    border-radius: 16777200px;
    box-sizing: border-box;
    display: flex;
    height: 48px;
    margin-top: 56px;
    width: 159.84px;
    cursor: pointer;
}

.div-subsection .button-3:hover {
    opacity: 0.96;
    /* reduce opacity on hover */
}

.div-subsection .text-wrapper-37 {
    color: #ffffff;
    font-family: "Inter", Helvetica;
    font-size: 16px;
    font-weight: 400;
    height: 24px;
    letter-spacing: 0.49px;
    line-height: 24px;
    margin-left: 48px;
    margin-top: 11.5px;
    white-space: nowrap;
    width: 64px;
}
</style>
