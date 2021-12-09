<template>
    <section>
        <div class="container py-5">
            <!-- Titles -->
            <div class="text-center py-5">
                <h3>Let's Dream Big Together</h3>
                <h2 class="fw-bold px-5 py-3">We are pioneers of the digital approach, using leading-edge technology to simplify procedures and apply executive coaching in the new age of digitalization.</h2>
            </div>
            <!-- Features List -->
            <ul class="row">
                <li 
                    class="col-4 px-2 py-3 d-flex"
                    v-for="(feature, index) in featuresList"
                    :key="`feature-${index}`"
                >
                    <div class="left text-center flex-shrink-0">
                        <i :class="feature.icon"></i>
                    </div>
                    <div class="right flex-grow-1">
                        <h4>{{ feature.title }}</h4>
                        <p>{{ feature.desc }}</p>
                    </div>
                </li>
            </ul>
            <!-- Buttons -->
            <div class="buttons text-center pt-3 pb-5">
                <button class="btn btn-secondary mx-3">
                    Learn more
                </button>
                <button class="btn btn-primary mx-3">
                    Get started today
                </button>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    name: 'Features',
    data() {
        return {
            featuresList: [
                {
                    title: 'One to One',
                    desc: 'Getting the necessary clarity about the current state to help you improve your game.',
                    icon: 'far fa-lightbulb'
                },
                {
                    title: 'Anywhere',
                    desc: 'Access to valuable and portable program which allow you to setup and live anywhere you want.',
                    icon: 'fas fa-map-marker-alt'
                },
                {
                    title: 'On Time',
                    desc: "Punctuality is our top priority because it's an essential criteria to assess a program quality.",
                    icon: 'far fa-clock'
                },
                {
                    title: 'Online Courses',
                    desc: 'Online business coaching now offers you a very powerful way to empower your business into success. ',
                    icon: 'fas fa-laptop'
                },
                {
                    title: 'Consulting',
                    desc: 'You will get a clear sense of direction for your business, thorough assessment and faster results.',
                    icon: 'fas fa-life-ring'
                },
                {
                    title: 'Self Development',
                    desc: 'Business Coaching often keep your focus and develop you both in a professional and personal way.',
                    icon: 'fas fa-cog'
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

// GENERAL
ul {
    list-style: none;
}

// COMPONENT
section {
    background: #fff;

    h2 {
        color: $main;
    }

    h3 {
        color: $secondary;
    }

    ul.row .left {
        width: 100px;
        font-size: 2rem;
    }
}

</style>