<template>
    <section class="container-fluid">
        <!-- Titles -->
        <TitleSection h2="What make they love us?" h3="People are praising Maxcoach" class="py-4"/>
        <!-- Reviews list -->
        <div class="row">
            <div class="col-4">
                <div class="review-card">

                </div>
            </div>
        </div>
        <!-- Page selector -->
        <PageSelector :numPages="4"/>
    </section>
</template>

<script>
import TitleSection from "@/components/TitleSection.vue";
import PageSelector from "@/components/PageSelector.vue";

export default {
    name: 'Reviews',
    components: {
        TitleSection,
        PageSelector
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/vars.scss";

section {
    background: $secondary-bg;
}
</style>