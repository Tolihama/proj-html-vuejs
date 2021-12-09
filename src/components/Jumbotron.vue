<template>
    <section>
        <img
            class="background"
            src="../assets/Jumbotron/home-business-hero-global-image.png" 
            alt="Jumbotron background"
        >
        <div class="container d-flex align-items-center">
            <div class="col-5 p-3">
                <h3 class="h4">New Challenges, New Skills</h3>
                <h2 class="text-uppercase fw-bold py-4">Build your own life coaching business</h2>
                <h4 class="h5 pb-4">Whole-life Business Coaching for committed entrepreneurs</h4>
                <button class="btn btn-primary">
                    Get started today
                </button>
            </div>
            <div class="col-7 text-center pt-5">
                <img src="../assets/Jumbotron/home-business-hero-avatar.png" alt="Jumbotron">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Jumbotron'
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

section {
    background-color: #eff2f6;
    position: relative;

    .background {
        position: absolute;
        left: 50%;
        z-index: 1;
    }

    div.container {
        position: relative;
        z-index: 2;

        h2 {
            color: $main;
            font-size: 3rem;
        }

        h3 {
            color: $secondary;
            font-weight: 600;
        }

        h4 {
            color: $tertiary;
            font-weight: 400;
            line-height: 2rem;
        }
    }
}

</style>