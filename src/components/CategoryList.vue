<template>
    <div class="category-list">
        <ul>
            <li v-for="(category, index) in list" :key="`category-${index}`">
                <a href="#" class="category-list__item" :title="category.name">
                    <div
                        class="category-list__pic"
                        :style="`background-image: url(${category.img})`"
                    ></div>
                    <div class="category-list__name">
                        {{ category.name }}
                    </div>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: ["list"],
};
</script>

<style lang="scss">
.category-list {
    ul {
        display: flex;
        flex-wrap: wrap;
        margin: -20px;
    }

    li {
        padding: 20px;
    }

    &__item {
        height: 100px;
        padding-right: 35px;
        display: flex;
        align-items: center;
        border-radius: 64px;
        background-color: $color-5;
        color: $color-4;
    }

    &__pic {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }

    &__name {
        margin-left: 24px;
        font-size: 35px;
        line-height: 40px;
        letter-spacing: -0.02em;
    }
}
</style>
