<template>
    <section>
        <div class="container pt-5">
            <!-- Titles -->
            <TitleSection
                h2="Upcoming Events"
                h3="Wanna transform your life?"
                class="py-5"
            />
            <!-- Cardlist events -->
            <div class="row flex-wrap">
                <!-- Card event -->
                <div
                    class="col-6 p-3"
                    v-for="(event, index) in eventList"
                    :key="`event-${index}`"
                >
                    <div class="event d-flex py-4 px-3">
                        <div class="event-details px-3 py-1 flex-grow-1">
                            <div class="where pb-2">{{ event.location }}</div>
                            <div class="title-event">{{ event.name }}</div>
                        </div>
                        <div
                            class="event-date d-flex flex-column px-3 py-1 flex-shrink-0 text-center"
                        >
                            <div class="day">{{ event.day }}</div>
                            <div class="month text-uppercase py-2">
                                {{ event.month }}
                            </div>
                            <div class="btn btn-primary">Get ticket</div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- All events -->
            <div class="view-all text-center py-4">
                Excited about our event? 
                <a href="#">View all events <i class="fas fa-long-arrow-alt-right"></i></a>
            </div>
        </div>
        <!-- Bottom svg -->
        <div class="bottom-svg">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 200">
                <path
                    d="M 720, 200
                    C 720, 200
                    1100, 200
                    1440, 0
                    L 1440, 200
                    L 720, 200"
                >
                </path>
            </svg>
        </div>
    </section>
</template>

<script>
import TitleSection from "@/components/TitleSection.vue";

export default {
    name: "Events",
    components: {
        TitleSection,
    },
    data() {
        return {
            eventList: [
                {
                    name: "Storytelling Workshop",
                    location: "Texas, US",
                    day: "22",
                    month: "Nov",
                },
                {
                    name: "Painting Art Contest 2020",
                    location: "New York, US",
                    day: "10",
                    month: "Oct",
                },
                {
                    name: "International Art Fair 2020",
                    location: "Hamburg, Germany",
                    day: "23",
                    month: "Nov",
                },
                {
                    name: "Street Performance: Call for Artist",
                    location: "Illinois, US",
                    day: "15",
                    month: "Dec",
                },
                {
                    name: "Consumer Food Safety Education Conference",
                    location: "Illinois, US",
                    day: "22",
                    month: "Jul",
                },
                {
                    name: "How meditation improve your mental health?",
                    location: "Dubai",
                    day: "12",
                    month: "Aug",
                },
            ],
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

section {
    background: $main-bg;
    position: relative;

    // Bottom svg
    .bottom-svg {
        position: absolute;
        bottom: 0;
        z-index: 0;

        svg {
            fill: #f8f8f8;
        }
    }

    .container {
        position: relative;
        padding-bottom: 100px;
        z-index: 1;
    }
}

// Event card
.event {
    position: relative;
    background: $secondary-bg;
    border-radius: 10px;
    transition: all .5s;
    overflow: hidden;
    cursor: pointer;

    &::before {
        content: '';
        position: absolute;
        width: 4px;
        height: 100%;
        left: 0;
        top: 0;
        background: $secondary;
        opacity: 0;
        transition: opacity .5s;
    }

    &:hover {
        background: $main-bg;
        box-shadow: 0 0 15px 1px rgba(100, 100, 100, 0.2);

        &::before {
            opacity: 1;
        }

        .btn {
            background: $secondary-hover;
        }
    }

    // Card left
    .event-details {
        .where {
            color: $tertiary;

            &::before {
                content: "\f3c5";
                font-family: "Font Awesome 5 Free";
                font-weight: 700;
                margin-right: 0.5rem;
            }
        }

        .title-event {
            color: $main;
            font-size: 1.5rem;
            font-weight: 700;
        }
    }

    // Card right
    .event-date {
        .day {
            color: $secondary;
            font-size: 3.5rem;
            line-height: 3.5rem;
            font-weight: 500;
        }

        .month {
            font-size: 1.2rem;
            font-weight: 700;
        }

        .btn {
            padding-top: 0.4rem;
            padding-bottom: 0.4rem;
        }
    }
}

// View all events
.view-all {
    color: $tertiary;
    font-size: 1.3rem;
    font-weight: 600;

    a {
        text-decoration: none;
        border-bottom: 1px solid #e0e0e0;
        color: $secondary;
    }
}
</style>
