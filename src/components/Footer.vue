<template>
    <footer>
        <div class="container p-5">
            <!-- Lists row -->
            <div class="row pb-3">
                <div class="col-6">
                    <h5 class="fw-bold">Address</h5>
                    <div class="py-2">
                        382 NE 111st St # 87394 Miami, FL 33179-3899
                    </div>
                    <div class="py-2">
                        +1(305) 547-9909 (9am - 5pm EST, Monday - Friday)
                    </div>
                    <div class="py-2">
                        support@maxcoach.com
                    </div>
                    <div class="social pt-4">
                        <i class="fab fa-facebook-square"></i>
                        <i class="fab fa-twitter"></i>
                        <i class="fab fa-instagram"></i>
                        <i class="fab fa-linkedin"></i>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row">
                        <div class="col-8">
                            <h5 class="fw-bold">Explore</h5>
                            <div class="row flex-wrap pb-3">
                                <div class="col-6 py-2">
                                    Start here
                                </div>
                                <div class="col-6 py-2">
                                    Success Story
                                </div>
                                <div class="col-6 py-2">
                                    Blog
                                </div>
                                <div class="col-6 py-2">
                                    Courses
                                </div>
                                <div class="col-6 py-2">
                                    About us
                                </div>
                                <div class="col-6 py-2">
                                    Contact us
                                </div>
                            </div>
                        </div>
                        <div class="col-4">
                            <h5 class="fw-bold">Information</h5>
                            <div class="py-2">
                                Membership
                            </div>
                            <div class="py-2">
                                Purchase guide
                            </div>
                            <div class="py-2">
                                Privacy policy
                            </div>
                            <div class="py-2">
                                Terms of service
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
    name: 'Footer'
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
}

.social {
    & > i {
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