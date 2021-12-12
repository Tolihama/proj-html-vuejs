<template>
    <div class="pages pb-5 d-flex justify-content-center">
        <div 
            class="page"
            v-for="n in numPages"
            :key="n"
            :class="{ active: n === activePage }"
            @click="pageClicked(n)"
        >
        </div>
    </div>
</template>

<script>
export default {
    name: 'PageSelector',
    props: {
        numPages: Number,
    },
    data() {
        return {
            activePage: 1,
        }
    },
    methods: {
        pageClicked(pageIndex) {
            this.activePage = pageIndex;
            this.$emit('selectedPage', pageIndex - 1);
        }
    }
}
</script>

<style lang="scss" scoped>
.pages .page {
    height: 10px;
    width: 10px;
    border-radius: 50%;
    background: #d8d8d8;
    margin: 0 .9rem;
    cursor: pointer;
    transition: all .5s;

    &.active,
    &:hover {
        transform: scale(2);
        background: #111111;
    }
}
</style>