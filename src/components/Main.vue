<template>
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
</template>

<script>
import Jumbotron from '@/components/Jumbotron.vue';
import Features from '@/components/Features.vue';
import Carousel from '@/components/Carousel.vue';
import Courses from '@/components/Courses.vue';
import Video from '@/components/Video.vue';
import Events from '@/components/Events.vue';
import Reviews from '@/components/Reviews.vue';
import Newsletter from '@/components/Newsletter.vue';

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Features,
        Carousel,
        Courses,
        Video,
        Events,
        Reviews,
        Newsletter,
    }
}
</script>

<style lang="scss" scoped>
main {
        padding-top: 90px;
}
</style>