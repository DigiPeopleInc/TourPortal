<template>
    <div class="more-list">
        <ul>
            <li>
                <div class="more-list__label">{{ label }}:</div>
            </li>
            <li v-for="(item, index) in list" :key="`item-${index}`">
                <a href="#" :title="item"
                    ><span>{{ item }}</span></a
                >
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: ["label", "list"],
};
</script>

<style lang="scss">
.more-list {
    overflow: hidden;

    ul {
        display: flex;
        flex-wrap: wrap;
        align-items: baseline;
        margin: -4px 0 -4px -17px;
    }

    li {
        display: flex;
        padding: 4px 0;
    }

    li:first-child {
        margin-right: 8px;
    }

    li:not(:nth-child(2))::before {
        align-self: center;
        font-size: 18px;
        line-height: 24px;
        letter-spacing: -0.02em;
        content: "·";
        color: $color-4;
        margin: 0 8px;
    }

    &__label {
        font-family: $font-2;
        color: $color-1;
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
    }

    span {
        font-weight: bold;
        font-size: 18px;
        line-height: 24px;
        color: $color-4;
        border-bottom: 1px solid rgba($color-1, 0.3);
    }
}
</style>
