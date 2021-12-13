<template>
    <div id="app">
        <!-- Header -->
        <Header :data="headerData" />

        <!-- Main -->
        <Main />

        <!-- Footer -->
        <Footer :data="footerData"/>
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
@import './styles/vars.scss';
@import './styles/buttons.scss';

// GENERAL APP
#app {
    min-height: 100vh;
}
</style>