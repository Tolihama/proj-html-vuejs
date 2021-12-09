<template>
    <section>
        <div class="container">
            <!-- Titles -->
            <div class="text-center pt-5">
                <h3>Let's Dream Big Together</h3>
                <h2 class="fw-bold px-5 py-3">Explore How can I help you</h2>
            </div>
            <!-- Cards -->
            <div class="cards py-3">
                <ul class="row d-flex py-3">
                    <li
                        v-for="(item, index) in list"
                        :key="`carousel-${index}`"
                        class="col-4 p-3"
                    >
                        <div class="card h-100 d-flex flex-column">
                            <div class="card-image">
                                <img 
                                    :src="require(`../assets/Carousel/${item.img}.jpg`)" 
                                    :alt="item.title"
                                    class="w-100"
                                >
                            </div>
                            <div class="card-text d-flex flex-column flex-grow-1 text-center p-3">
                                <h4 class="fw-bold py-3">{{ item.title }}</h4>
                                <p class="flex-grow-1 py-2">{{ item.desc }}</p>
                            </div>
                            <div class="discover text-center py-3">
                                Discover now
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    name: 'Carousel',
    data() {
        return {
            list: [
                {
                    img: 'home-business-service-slide-01-480x298',
                    title: 'Consultative Training',
                    desc: 'With a coach addressing multiple issues that are off balance, affecting your business in various unconsidered ways.'
                },
                {
                    img: 'home-business-service-slide-02-480x298',
                    title: 'Reak Deal Coaching',
                    desc: 'Brings an exceptionally powerful opportunity. Being able to accept, to work with that opportunity.'
                },
                {
                    img: 'home-business-service-slide-03-480x298',
                    title: 'Advisor Training Program',
                    desc: 'Getting high quality, entrepreneur mindset driven online business coaching, is what is needed.'
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

ul {
    list-style: none;
}

section {
    background-color: $secondary-bg;

    h2 {
        font-size: 3rem;
    }

    h3 {
        color: $secondary;
    }
}

.card {
    border-radius: 5px;
    box-shadow: 0 0 15px rgba(0,0,0,.2);
    overflow: hidden;

    &:hover {
        cursor: pointer;

        .card-image img {
            transform: scale(110%);
        }

        .discover {
            color: #fff;
            background: $secondary;
        }
    }

    .card-image {
        overflow: hidden;

        img {
            transform: scale(100%);
            transition: transform 1s;
        }
    }
    
    .card-text {
        & > * {
            margin: 0;
        }

        p {
            color: $tertiary;
            font-size: 1.2rem;
        }
    }

    .discover {
        border-top: 1px solid $main-border;
        color: $secondary;
        font-weight: 700;
        transition: all 1s;

        &::after {
            content: '\f30b';
            font-family: 'Font Awesome 5 Free';
            font-weight: 700;
            margin-left: 6px;
            vertical-align: middle;
        }
    }

}

</style>