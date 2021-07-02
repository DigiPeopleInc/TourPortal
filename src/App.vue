<template>
    <div id="app">
        <layout-header></layout-header>
        <main-section></main-section>
        <category-section></category-section>
        <layout-footer></layout-footer>
    </div>
</template>

<script>
import LayoutHeader from "@/components/LayoutHeader";
import LayoutFooter from "@/components/LayoutFooter";
import MainSection from "@/components/MainSection";
import CategorySection from "@/components/CategorySection";

export default {
    name: "App",
    components: {
        LayoutHeader,
        MainSection,
        CategorySection,
        LayoutFooter,
    },
};
</script>

<style lang="scss">
@import "~destyle.css/destyle.css";
@import "@/assets/styles/fonts";

html {
    font-family: $font-1;
}

body {
    background-color: $color-3;
}
</style>
