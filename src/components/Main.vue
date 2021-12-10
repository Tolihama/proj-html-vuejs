<template>
    <main>
        <Jumbotron />
        <Features />
        <Carousel />
        <Courses />
        <Testimonial />
    </main>
</template>

<script>
// IMPORT COMPONENTS
import Jumbotron from '@/components/Jumbotron.vue';
import Features from '@/components/Features.vue';
import Carousel from '@/components/Carousel.vue';
import Courses from '@/components/Courses.vue';
import Testimonial from '@/components/Testimonial.vue';

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Features,
        Carousel,
        Courses,
        Testimonial
    }
}
</script>

<style scoped lang="scss">
main {
    padding-top: 90px;
}
</style>