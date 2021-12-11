<template>
    <div id="app">
        <Header />
        <Main />
        <Footer />
    </div>
</template>

<script>
// Import components
import Header from '@/components/Header.vue';
import Main from '@/components/Main.vue';
import Footer from '@/components/Footer.vue';

export default {
    name: "App",
    components: {
        Header,
        Main,
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
}
</style>