<template>
    <Layout>
        <LandingPageMasthead />
    </Layout>
</template>

<script>
    import LandingPageMasthead from '~/components/LandingPageMasthead.vue';

    export default {
        metaInfo: {
            title: 'Hello, world!'
        },

        components: {
            LandingPageMasthead,
        }
    }
</script>
