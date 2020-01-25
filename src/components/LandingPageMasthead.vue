<template>
    <section class="containerMasthead">
        <span class="logoContainer">
            <g-image
                src="~/assets/kh-logo-white.png"
                class="logo"
            />
        </span>
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
                please fill out the form below and we’ll get back to you within 48 hours.
            </p>
        </div>
    </section>
</template>

<style scoped>
    .containerMasthead {
        background-image:
            url("../assets/kelsey-horner-photo.jpg"),
            linear-gradient(rgba(0,0,0,0.5), rgba(0, 0, 0, .1));
        background-position: center 0 bottom 10rem;
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
        width: 20rem;
    }

    .containerText {
        align-items: center;
        color: #fff;
        display: flex;
        flex-direction: column;
        height: 75%;
        justify-content: center;
    }

    .welcomeText {
        font-family: 'Quentin';
        font-size: 3.5rem;
        letter-spacing: .5rem;
        margin: 0 0 -.5rem;
    }

    .underConstructionText {
        font-size: 1.5rem;
        letter-spacing: .1rem;
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
        width: 24rem;
        text-align: center;
    }
</style>