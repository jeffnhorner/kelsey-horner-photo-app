<template>
    <section>
        <div v-bind:class="[,
                { 'containerMasthead' : !isHandheld },
                { 'containerMastheadMobile' : isHandheld }
            ]
        ">
            <span class="logoContainer">
                <g-image
                    src="~/assets/kh-logo-white.png"
                    class="logo"
                />
            </span>
            <g-image
                src="~/assets/kelsey-horner-photo.jpg"
                class="mobilePhoto"
            />
            <div class="containerText">
                <h3 class="welcomeText">good things take time</h3>
                <p class="underConstructionText">website under construction</p>
                <span class="socialIcons">
                    <a
                        class="socialLinks"
                        href="https://www.instagram.com/kelseyhornerphoto"
                        target="_blank"
                    >
                        <font-awesome
                            v-bind:icon="['fab', 'instagram']"
                            size="2x"
                        />
                    </a>
                    <a
                        class="socialLinks"
                        href="https://www.facebook.com/kelseyhornerphotography"
                        target="_blank"
                    >
                        <font-awesome
                            v-bind:icon="['fab', 'facebook-square']"
                            size="2x"
                        />
                    </a>
                </span>
                <p class="formText">
                    please fill out the form below and we’ll get back to you within 48 hours!
                </p>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        created () {
            console.log(this.$mq);
        },

        computed: {
            isHandheld () {
                return this.$mq === 'xs' || this.$mq === 'sm';
            }
        }
    }
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css?family=Mr+Dafoe&display=swap');

    @media only screen and (min-width: 567px) {
        .mobilePhoto {
            display: none;
        }
    }

    .containerMasthead {
        background-image:
            url("../assets/kelsey-horner-photo.jpg"),
            linear-gradient(rgba(0,0,0,0.5), rgba(0, 0, 0, .1));
        background-position: center;
        background-repeat:  no-repeat;
        background-attachment: fixed;
        background-size:  cover;
        background-blend-mode: overlay;
        height: 100vh;
        width: 100%;
    }

    .logoContainer {
        display: flex;
        justify-content: center;
        padding-top: 3rem;
    }

    .logo {
        width: 100%;
        height: 100%;
        max-width: 20rem;
    }

    .containerText {
        align-items: center;
        color: #fff;
        display: flex;
        flex-direction: column;
        height: 75%;
        justify-content: center;
        text-align: center;
    }

    .welcomeText {
        font-family: 'Quentin', 'Mr Dafoe', cursive;
        font-size: 4rem;
        margin: 0 0 -.5rem;
    }

    .underConstructionText {
        font-size: 1.5rem;
        letter-spacing: .2rem;
        margin: 0;
    }

    .socialIcons {
        display: flex;
        justify-content: space-between;
        margin: 1rem 0;
        width: 4.5rem;
    }

    .socialLinks {
        color: #efefef;
        transition: .2s ease-in-out;
    }

    .socialLinks:visited {
        color: #efefef;
    }

    .socialLinks:hover {
        opacity: .8;
    }

    .formText {
        color: #efefef;
        font-size: 1rem;
        letter-spacing: .1rem;
        margin: 0;
        width: 100%;
        max-width: 24rem;
        text-align: center;
    }

    @media only screen and (max-width: 768px) {
        .welcomeText {
            font-size: 2.5rem;
        }
    }

    @media only screen and (max-width: 567px) {
        section {
            height: 28rem;
        }

        .containerMastheadMobile {
            height: 100%;
            overflow: hidden;
            position: relative;
        }

        .mobilePhoto {
            display: block;
            height: auto;
            margin-top: -5rem;
            position: absolute;
            width: 43rem;
            z-index: -1;
        }

        .overlay:before {
            display: block;
            height: 100%;
            width: 100%;
            position: absolute;
            background: #000;
            content: '';
            top: 0;
            right: 0;
            opacity: .25;
        }

        .containerMasthead {
            background-position: bottom right 66%;
        }

        .logoContainer {
            padding-top: 2rem;
        }

        .logo {
            width: 100%;
            max-width: 14rem;
        }

        .containerText {
            margin-top: 1.5rem;
        }

        .welcomeText {
            font-size: 1.85rem;
            text-align: center;
        }

        .underConstructionText {
            font-size: 1.1rem;
            text-align: center;
            margin-top: 1rem;
            width: 100%;
            max-width: 20rem;
        }

        .formText {
            font-size: .875rem;
        }
    }

    @media only screen and (max-width: 414px) {
        .containerMasthead {
            background-position: bottom 200px right 66%;
            height: 75vh;
            background-size: cover;
        }

        .underConstructionText {
            letter-spacing: .15rem;
        }

        .formText {
            width: 100%;
            max-width: 17rem;
        }
    }
</style>