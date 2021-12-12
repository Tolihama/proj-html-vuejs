<template>
    <div class="text-center pt-5">
        <h3>Let's Dream Big Together</h3>
        <h2 class="fw-bold px-5 py-3">Explore How can I help you</h2>
    </div>
</template>

<script>
export default {
    name: 'TitleSection',
    props: {
        h2: String,
        h3: String,
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

h2 {
    font-size: 3rem;
}

h3 {
    color: $secondary;
}
</style>