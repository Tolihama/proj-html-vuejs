<template>
    <section class="container-fluid py-5">
        <!-- Titles -->
        <TitleSection h2="Explore How can I help you" h3="Let's Dream Big Together" />
        <!-- CARDS -->
        <div class="cards row">
            <div 
                class="col-3 px-4"
                v-for="n in 4"
                :key="n"
            >
                <div class="card">
                    <img src="../assets/Courses/course-02-443x600.jpg" alt="Course">
                    <div class="card-text p-4 d-flex flex-column justify-content-end">
                        <div class="course-price fw-bold">
                            <span class="price-integer fs-2">$40.</span>
                            <span class="price-decimals fs-4">00</span>
                        </div>
                        <div class="course-name fs-3 fw-bold pb-2">
                            Learning to Write as a professional Author
                        </div>
                        <div class="course-details">
                            <div class="course-info d-flex py-2 fs-5">
                                <div class="lessons"><i class="far fa-file-alt"></i> 20 Lessons</div>
                                <div class="students ps-5"><i class="far fa-user"></i> 50 Students</div>
                            </div>
                            <div class="course-description">
                                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sint reiciendis ullam eos laudantium iste officia, sapiente placeat doloremque animi delectus accusantium porro facere ea. Molestiae obcaecati voluptates aut quidem voluptas.
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
        <!-- View all courses -->
        <div class="view-all text-center fs-5">
            Take the control of their life back and start doing things to make their dream come true.
            <a href="#">View all courses <i class="fas fa-long-arrow-alt-right"></i></a>
        </div>

    </section>
</template>

<script>
import TitleSection from '@/components/TitleSection.vue';

export default {
    name: 'Courses',
    components: {
        TitleSection,
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

section {
    background: #fff;
}

.cards {
    padding: 2rem 10rem;
}

.card {
    position: relative;
    overflow: hidden;
    border-radius: 10px;

    img {
        width: 100%;
        object-fit: cover;
    }

    .card-text {
        position: absolute;
        height: 100%;
        top: 0;
        left: 0;
        z-index: 1;
        background: linear-gradient(
            to top,
            rgba(0,0,0,1) 0%,
            rgba(0,0,0,.5) 25%,
            rgba(0,0,0,.25) 50%,
            rgba(0,0,0,0) 100%
        );
        color: #fff;
        transition: all 1s;
        cursor: pointer;

        .course-price {
            color: $secondary;
        }

        .course-name {
            line-height: 2.5rem;
        }

        .course-details {
            display: none;
        }

        &:hover {
            background: linear-gradient(
                to top,
                rgba(0,0,0,1) 0%,
                rgba(0,0,0,.5) 50%,
                rgba(0,0,0,0) 100%
            );

            .course-details {
                display: block;
            }
        }
    }
}

.view-all {
    color: $tertiary;
    font-weight: 600;
    padding: 1rem 35%;

    a {
        text-decoration: none;
        border-bottom: 1px solid #e0e0e0;
        color: $main;
    }
}
</style>