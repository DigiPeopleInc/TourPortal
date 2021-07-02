<template>
    <button :type="type" :class="['custom-button', theme]">{{ text }}</button>
</template>

<script>
export default {
    props: ["text", "value", "type", "theme"],
};
</script>

<style lang="scss">
.custom-button {
    display: block;
    width: 100%;
    height: 80px;
    font-weight: 500;
    font-size: 20px;
    line-height: 24px;
    letter-spacing: -0.02em;
    border-radius: 8px;
    text-align: center;

    &.primary {
        color: $color-5;
        background-color: $color-1;
    }
}
</style>
