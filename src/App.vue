<template>
    <div id="app">
        <!-- Header -->
        <Header :data="headerData" />

        <!-- Main -->
        <Main />

        <!-- Footer -->
        <Footer :data="footerData"/>

        <!-- Back to top fixed btn -->
        <div class="to-top">
            <a href="#">
                <i class="fas fa-long-arrow-alt-up"></i>
            </a>
        </div>
    </div>
</template>

<script>
// Import components
import Header from '@/components/Header.vue';

import Main from '@/components/Main.vue';

import Footer from '@/components/Footer.vue';

export default {
    name: "App",
    components: {
        Header,
        Main,
        Footer
    },
    data() {
        return {
            headerData: {
                menu: [
                    {
                        name: 'Home',
                        url: '#',
                        submenus: [
                            {
                                name: 'Link',
                                url: '#'
                            }
                        ]
                    },
                    {
                        name: 'Pages',
                        url: '#',
                        submenus: [
                            {
                                name: 'Link',
                                url: '#'
                            }
                        ]
                    },
                    {
                        name: 'Courses',
                        url: '#',
                        submenus: [
                            {
                                name: 'Link',
                                url: '#'
                            }
                        ]
                    },
                    {
                        name: 'Features',
                        url: '#',
                        submenus: [
                            {
                                name: 'Link',
                                url: '#'
                            }
                        ]
                    },
                    {
                        name: 'Shop',
                        url: '#',
                        submenus: [
                            {
                                name: 'Link',
                                url: '#'
                            }
                        ]
                    }
                ],
                languages: [
                    {
                        text: 'english',
                        img: 'en',
                    },
                    {
                        text: 'german',
                        img: 'de',
                    },
                    {
                        text: 'francais',
                        img: 'fr',
                    },
                ],
            },

            footerData: {

                address: [
                    '382 NE 111st St # 87394 Miami, FL 33179-3899',
                    '+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)'
                ],

                email: 'support@maxcoach.com',

                social: [
                    {
                        socialName: 'Facebook',
                        icon: 'fab fa-facebook-square',
                        url: '#',
                    },
                    {
                        socialName: 'Twitter',
                        icon: 'fab fa-twitter',
                        url: '#',
                    },
                    {
                        socialName: 'Instagram',
                        icon: 'fab fa-instagram',
                        url: '#',
                    },
                    {
                        socialName: 'Linkedin',
                        icon: 'fab fa-linkedin',
                        url: '#',
                    },
                ],

                explore: [
                    {
                        linkName: 'Start here',
                        url: '#',
                    },
                    {
                        linkName: 'Success Story',
                        url: '#',
                    },
                    {
                        linkName: 'Blog',
                        url: '#',
                    },
                    {
                        linkName: 'Courses',
                        url: '#',
                    },
                    {
                        linkName: 'About us',
                        url: '#',
                    },
                    {
                        linkName: 'Contact us',
                        url: '#',
                    },
                ],

                information: [
                    {
                        linkName: 'Membership',
                        url: '#',
                    },
                    {
                        linkName: 'Purchase guide',
                        url: '#',
                    },
                    {
                        linkName: 'Privacy policy',
                        url: '#',
                    },
                    {
                        linkName: 'Terms of service',
                        url: '#',
                    },
                ],
            },
        }
    }
};
</script>

<style lang="scss">
// IMPORTS
@import './styles/globals.scss';
@import './styles/vars.scss';
@import './styles/buttons.scss';

// GENERAL APP
#app {
    min-height: 100vh;
    position: relative;
}

.to-top a {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    right: 40px;
    bottom: 40px;
    height: 80px;
    width: 80px;
    border-radius: 50%;
    background: $btn-bg-primary;
    overflow: hidden;

    i {
        font-size: 2rem;
        color: $btn-color-primary;
    }

    &:hover i {
        animation: arrow 1s;
    }
}

@keyframes arrow {
    0% {transform: translateY(0)}
    49% {transform: translateY(-200%)}
    50% {opacity: 0}
    51% {transform: translateY(200%)}
    100% {transform: translateY(0)}
}
</style>