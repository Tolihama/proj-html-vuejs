<template>
    <footer>
        <div class="container p-5">
            <!-- Lists row -->
            <div class="row pb-3">
                <div class="col-6">
                    <h5 class="fw-bold">Address</h5>
                    <div 
                        v-for="(addressline, i) in data.address"
                        :key="`addressline-${i}`"
                        class="py-2"
                    >
                        {{addressline}}
                    </div>
                    <div class="py-2 email">
                        <a :href="`mailto:${data.email}`">{{data.email}}</a>
                    </div>
                    <div class="social pt-4">
                        <a
                            v-for="social in data.social"
                            :key="`social-${social.socialName}`"
                            :href="social.url"
                        >
                            <i :class="social.icon"></i>
                        </a>

                    </div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div class="col-8">
                            <h5 class="fw-bold">Explore</h5>
                            <div class="row flex-wrap pb-3">
                                <div 
                                    v-for="(link, i) in data.explore"
                                    :key="`explore-${i}`"
                                    class="col-6 py-2"
                                >
                                    <a :href="link.url">{{ link.linkName }}</a>
                                </div>
                            </div>
                        </div>
                        <div class="col-4">
                            <h5 class="fw-bold">Information</h5>
                            <div 
                                v-for="(link, i) in data.information"
                                :key="`information-${i}`"
                                class="py-2"
                            >
                                <a :href="link.url">{{ link.linkName }}</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Copyright row -->
            <div class="row pt-5">
                <div class="col-12 text-center">
                    &copy; 2020 Maxcoach. All Rights Reserved
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        data: Object,
    }
}
</script>

<style scoped lang="scss">
footer {
    background: #171621;
    color: #ababab;
    font-weight: 600;

    h5 {
        color: #fff;
    }

    a {
        text-decoration: none;
        color: currentColor;
        transition: all .3s;

        &:hover {
            color: #666;
        }
    }
}

.social {
    & > a {
        font-size: 1.6rem;
        padding: 0 1rem;

        &:first-child {
            padding: 0 1rem 0 0;
        }

        &:last-child {
            padding: 0 0 0 1rem;
        }
    }
}
</style>