<template>
    <section>
        <img class="bg bg-shape-1" src="../assets/Newsletter/maxcoach-shape-02.png" alt="Background Shape 1">
        <img class="bg bg-shape-2" src="../assets/Newsletter/maxcoach-shape-09.png" alt="Background Shape 1">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-6 text-center">
                    <h2 class="title-newsletter">
                        Subscribe <span class="secondary-title">Newsletter</span>
                    </h2>
                    <h3 class="subtitle-newsletter pt-4 pb-5">
                        Enter your email address to register to out newsletter subscription delivered on a regular basis!
                    </h3>
                    <div class="d-flex">
                        <input type="email" placeholder="Enter your email" class="flex-grow-1">
                        <button class="btn btn-primary">Subscribe</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Newsletter'
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

section {
    background: $bg-section-type-1;
    position: relative;

    .container {
        padding: 5rem 2rem;
    }

    .bg {
        position: absolute;

        &.bg-shape-1 {
            top: 50%;
            right: 20%;
            transform: translateY(-50%);
            z-index: 1;
        }

        &.bg-shape-2 {
            top: 40%;
            right: 20%;
            transform: translateY(-50%);
        }
    }
}

.title-newsletter {
    font-size: 3rem;
    letter-spacing: .1rem;
    font-weight: 700;

    .secondary-title {
        color: $secondary-text;
        font-weight: 400;
    }
}

.subtitle-newsletter {
    color: #696969;
    font-size: 1.3rem;
    font-weight: 600;
}

// Button special style for component
.btn {
    border-radius: 0 10px 10px 0;
}

input {
    border: none;
    background: #f5f5f5;
    padding: 0 2rem;
    border-radius: 10px 0 0 10px;
}
</style>