<template>
    <section class="container-fluid">
        <img
            class="background"
            src="../assets/Testimonial/background-map-dots-top-right-transparent.png"
            alt="Testimonial Section Background"
        />
        <img
            class="square-background"
            src="../assets/Testimonial/maxcoach-shape-07-150x150.png"
            alt="Square Shape Background"
        />
        <div class="row align-items-center">
            <div class="col-5 px-5">
                <div class="video">
                    <img
                        class="video-preview"
                        src="../assets/Testimonial/home-business-video-poster-670x450.jpg"
                        alt="Video"
                    />
                    <img
                        class="youtube-logo"
                        src="../assets/Testimonial/icon-youtube-play.png"
                        alt="YouTube"
                    />
                </div>
            </div>
            <div class="col-7 px-5">
                <div class="faq pe-5">
                    <h2 class="fw-bold">
                        To Thrive In Business Today, You'll Need a Good Plan
                    </h2>
                    <ul class="py-5">
                        <li v-for="(n, index) in 3" :key="n" class="py-3">
                            <div
                                :class="{ active: activeFaq === index }"
                                @click="setActive(index)"
                            >
                                <h5 class="question fw-bold">
                                    How can we help?
                                </h5>
                                <div
                                    class="text pt-3"
                                    v-show="activeFaq === index"
                                >
                                    <p>
                                        Lorem ipsum dolor sit amet
                                        consectetur adipisicing elit.
                                        Repellat officia illo, soluta
                                        labore, ratione non incidunt
                                        doloribus sint quo sit fugit
                                        nesciunt rem impedit praesentium
                                        consectetur dolorum temporibus quis
                                        aliquam!
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit amet
                                        consectetur adipisicing elit.
                                        Facilis praesentium aut suscipit
                                        itaque. Fuga deleniti expedita unde
                                        reprehenderit, corporis eveniet,
                                        possimus dolorem magni facere, odio
                                        harum veniam sequi doloribus
                                        laboriosam.
                                    </p>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Video",
    data() {
        return {
            activeFaq: 0,
        };
    },
    methods: {
        setActive(index) {
            if (this.activeFaq !== index) {
                this.activeFaq = index;
            }
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

section {
    position: relative;
    background: $bg-video-section;
    padding: 5rem 10rem;
    color: #fff;

    .background {
        position: absolute;
        top: 0;
        right: 0;
    }

    .square-background {
        position: absolute;
        bottom: 8%;
        transform: scale(150%);
    }
}

.video {
    position: relative;
    border-radius: 5px;
    overflow: hidden;

    .video-preview {
        width: 100%;
    }

    .youtube-logo {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}

.faq {
    h2 {
        font-size: 4rem;
    }

    ul {
        list-style: none;

        li {
            border-bottom: 2px solid #474556;
            padding-left: 3rem;
            overflow: hidden;

            h5 {
                transform: translateX(-3rem);
                margin: 0;
                font-size: 2rem;
                cursor: pointer;

                &::before {
                    content: "\f13a";
                    font-family: "Font Awesome 5 Free";
                    margin-right: 0.8rem;
                }

                &:hover {
                    color: $secondary-text;
                    transition: all 0.5s;
                }
            }

            .text {
                height: 0;
                padding: 0;
                overflow: hidden;
                font-size: 1.1rem;
                transition: all .5s;
            }

            .active {
                h5 {
                    color: $secondary-text;
                    transition: all 1s;

                    &::before {
                        content: "\f139";
                        font-family: "Font Awesome 5 Free";
                        margin-right: 0.8rem;
                    }
                }

                .text {
                    height: auto;
                }
            }
        }
    }
}
</style>