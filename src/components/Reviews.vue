<template>
    <section class="container-fluid">
        <!-- Titles -->
        <TitleSection h2="What make they love us?" h3="People are praising Maxcoach" class="pt-4"/>
        <!-- Reviews list -->
        <div class="row p-5">
            <!-- Review card -->
            <div 
                class="col-4 px-4"
                v-for="(review, index) in testimonialToPrint"
                :key="`review-${index}`"
            >
                <div class="review-card p-5" :class="{active : index === 1}">
                    <h4>{{ review.title }}</h4>
                    <p class="py-3">{{ review.desc }}</p>
                    <div class="testimonial d-flex">
                        <div class="testimonial-avatar">
                            <img :src="require(`../assets/Reviews/${review.avatar}.jpg`)" :alt="`${review.testimonialName} Avatar`">
                        </div>
                        <div class="testimonial-id ps-4 d-flex flex-column justify-content-center">
                            <h5 class="text-uppercase">{{ review.testimonialName }}</h5>
                            <h6>/ {{ review.testimonialJob }}</h6>
                        </div>
                    </div>

                </div>
            </div>
        </div>
        <!-- Page selector -->
        <PageSelector :numPages="testimonials.length" @selectedPage="setActivePage"/>
    </section>
</template>

<script>
import TitleSection from "@/components/TitleSection.vue";
import PageSelector from "@/components/PageSelector.vue";

export default {
    name: 'Reviews',
    components: {
        TitleSection,
        PageSelector
    },
    data() {
        return {
            testimonials: [
                {
                    title: 'High level of efficiency and scientific teaching methods',
                    desc: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    avatar: 'testimonial-avata-02',
                    testimonialName: 'Mina Hollace',
                    testimonialJob: 'Freelancer'
                },
                {
                    title: 'Professional team of specialist and passionate mentors at reach',
                    desc: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    avatar: 'testimonial-avata-03',
                    testimonialName: 'Madley Pondor',
                    testimonialJob: 'IT Specialist'
                },
                {
                    title: 'High level of efficiency and scientific teaching methods',
                    desc: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    avatar: 'testimonial-avata-04',
                    testimonialName: 'Mina Hollace',
                    testimonialJob: 'Freelancer'
                },
                {
                    title: "It's a choice of quality for people with special needs",
                    desc: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    avatar: 'testimonial-avata-01',
                    testimonialName: 'Florence Themes',
                    testimonialJob: 'Multimedia Admin'
                },
            ],
            activePage: 0,
        }
    },
    computed: {
        testimonialToPrint() {
            const testimonialToPrint = [];

            // Push active item
            testimonialToPrint.push(this.testimonials[this.activePage]);

            // Unshift before active item
            if (this.activePage === 0) {
                testimonialToPrint.unshift(this.testimonials[this.testimonials.length - 1]);
            } else {
                testimonialToPrint.unshift(this.testimonials[this.activePage - 1]);
            }

            // Push after active item
            if (this.activePage === this.testimonials.length - 1) {
                testimonialToPrint.push(this.testimonials[0]);
            } else {
                testimonialToPrint.push(this.testimonials[this.activePage + 1]);
            }

            return testimonialToPrint;
        }
    },
    methods: {
        setActivePage(activePage) {
            this.activePage = activePage;
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

section {
    background: $bg-section-type-2;
}

// Review card
.review-card {
    background: #fff;
    opacity: 0.5;

    &.active {
        opacity: 1;
    }

    h4 {
        color: #3f3a64;
        font-weight: 700;
    }

    p {
        color: $tertiary-text;
        font-size: 1.2rem;
    }

    .testimonial {
        .testimonial-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            overflow: hidden;

            img {
                width: 100%;
                height: 100%;
            }
        }

        .testimonial-id {
            h5 {
                color: #3f3a64;
                font-weight: 700;
                font-size: 1.2rem;
            }

            h6 {
                color: $tertiary-text;
                font-size: 1.1rem;
            }
        }
    }
}
</style>