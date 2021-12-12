<template>
    <div id="app">
        <!-- Header -->
        <Header />

        <!-- Main -->
        <main>
            <Jumbotron />
            <Features />
            <Carousel />
            <Courses />
            <Video />
            <Events />
            <Reviews />
            <Newsletter />
        </main>

        <!-- Footer -->
        <Footer />
    </div>
</template>

<script>
// Import components
import Header from '@/components/Header.vue';

import Jumbotron from '@/components/Jumbotron.vue';
import Features from '@/components/Features.vue';
import Carousel from '@/components/Carousel.vue';
import Courses from '@/components/Courses.vue';
import Video from '@/components/Video.vue';
import Events from '@/components/Events.vue';
import Reviews from '@/components/Reviews.vue';
import Newsletter from '@/components/Newsletter.vue';

import Footer from '@/components/Footer.vue';

export default {
    name: "App",
    components: {
        Header,
        Jumbotron,
        Features,
        Carousel,
        Courses,
        Video,
        Events,
        Reviews,
        Newsletter,
        Footer
    },
};
</script>

<style lang="scss">
// IMPORTS
@import './styles/vars.scss';
@import './styles/buttons.scss';

// GENERAL APP
#app {
    min-height: 100vh;

    main {
        padding-top: 90px;
    }
}
</style>