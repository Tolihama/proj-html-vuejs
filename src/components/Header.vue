<template>
    <header class="d-flex justify-content-between align-items-center w-100">
        <!-- LOGO -->
        <div class="logo h-100 d-flex align-items-center">
            <img class="h-50" src="../assets/Header/dark-logo.png" alt="Logo">
        </div>
        <!-- MAIN NAV -->
        <nav class="h-100">
            <ul class="d-flex align-items-center h-100">
                <li 
                    v-for="item in menu"
                    :key="`menu-${item.name}`"
                    class="menu h-100 d-flex flex-column justify-content-center"
                >
                    <a :href="item.url">
                        {{ item.name }}
                    </a>
                    <ul class="dropdown">
                        <li
                            v-for="subitem in item.submenus"
                            :key="`submenu-${item.name}-${subitem.name}`"
                            class="submenu p-3"
                        >
                            <a :href="subitem.url">
                                {{ subitem.name }}
                            </a>
                        </li>
                    </ul>
                </li>
            </ul>
        </nav>
        <!-- RIGHT HEADER: LANG AND SEARCH INPUT -->
        <div class="right h-100 d-flex align-items-center">
            <div class="lang menu h-100 d-flex align-items-center">
                <img 
                    :src="require(`../assets/Header/${activeLang.img}.png`)" 
                    :alt="`Flag ${activeLang.img}`"
                    class="px-3"
                >
                <span class="text-uppercase">
                    <strong>
                        {{ activeLang.text }}
                    </strong>
                </span>
                <i class="far fa-user-circle px-4"></i>
                <ul class="dropdown py-3">
                    <li
                        v-for="(lang, index) in languages"
                        :key="lang.text"
                        class="w-100 py-2 d-flex align-items-center"
                        @click="setLanguage(index)"
                    >
                        <img 
                            :src="require(`../assets/Header/${lang.img}.png`)" 
                            :alt="`Flag ${lang.img}`"
                            class="px-3 text-start"
                        >
                        <span class="text-uppercase flex-grow-1 px-3">
                            <strong>
                                {{ lang.text }}
                            </strong>
                        </span>
                    </li>
                </ul>
            </div>
            <div class="search h-100 px-5 d-flex align-items-center">
                <input 
                    type="text" 
                    placeholder="Search..."
                    class="me-3 p-2"
                >
                <i class="fas fa-search"></i>
            </div>

        </div>

    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
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
            activeLang: {
                text: 'english',
                img: 'en',
            },
        }
    },
    methods: {
        setLanguage(lang) {
            this.activeLang = this.languages[lang];
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

// GENERAL COMPONENT
header {
    position: fixed;
    height: 90px;
    background: #fff;
    border-bottom: 1px solid $main-border;
    box-shadow: 0 10px 10px 0 rgba(0,0,0,.1);
    z-index: 10;

    .logo {
        padding: .75rem 10rem;
    }
}

ul {
    list-style: none;
    padding: 0;
}

// MENU
.menu {
    position: relative;
    margin: 0 1.5rem;
    padding: 0 1rem;
    font-size: 1.25rem;

    a {
        text-decoration: none;
        color: $link;
    }

    & > a::after,
    & > span::after {
        content: '\f078';
        font-family: 'Font Awesome 5 Free';
        font-weight: 700;
        font-size: 1rem;
        margin-left: 6px;
    }

    .dropdown {
        position: absolute;
        opacity: 0;
        top: 100%;
        left: 0;
        width: 100%;
        background: #fff;
        box-shadow: 0 5px 5px rgba(0,0,0,.25);
        text-align: center;
        transform: translateY(25%);
        transition: all .5s;

        li:hover {
            background: $dropdown-hover;
            cursor: pointer;
        }
    }

    &:hover .dropdown {
        opacity: 1;
        transform: translateY(0);
    }
}

// RIGHT
.right {
    .lang {
        font-size: 1.1rem;
        padding: 0 0 0 1rem;
        margin: 0 0 0 1.5rem;
    }

    .search {
        border-left: 1px solid $main-border;

        input {
            border: none;
        }
    }
}

</style>