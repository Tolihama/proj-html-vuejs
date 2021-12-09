<template>
    <main>
        <Jumbotron />
        <Features />
    </main>
</template>

<script>
// IMPORT COMPONENTS
import Jumbotron from '@/components/Jumbotron.vue';
import Features from '@/components/Features.vue';

export default {
    name: 'Main',
    components: {
        Jumbotron,
        Features
    }
}
</script>

<style scoped lang="scss">
main {
    padding-top: 90px;
}
</style>