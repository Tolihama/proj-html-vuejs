<template>
    <main>
        <Jumbotron />
        <Features />
        <Carousel />
        <Courses />
    </main>
</template>

<script>
// IMPORT COMPONENTS
import Jumbotron from '@/components/Jumbotron.vue';
import Features from '@/components/Features.vue';
import Carousel from '@/components/Carousel.vue';
import Courses from '@/components/Courses.vue';


export default {
    name: 'Main',
    components: {
        Jumbotron,
        Features,
        Carousel,
        Courses
    }
}
</script>

<style scoped lang="scss">
main {
    padding-top: 90px;
}
</style>