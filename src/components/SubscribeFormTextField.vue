<template>
    <div :class="['subscribe-text-field', { filled: value }]">
        <label class="subscribe-text-field__label" :for="id">{{ label }}</label>
        <input
            type="text"
            class="subscribe-text-field__input"
            :value="value"
            :id="id"
            readonly
        />
    </div>
</template>

<script>
export default {
    props: ["label", "value"],
    data() {
        return {
            id: Math.random()
                .toString(36)
                .slice(2),
        };
    },
};
</script>

<style lang="scss">
.subscribe-text-field {
    position: relative;

    &__label {
        position: absolute;
        top: calc(50% - 12px);
        font-size: 20px;
        line-height: 24px;
        letter-spacing: -0.02em;
        color: $color-6;
        pointer-events: none;
        padding: 0 16px;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;

        .filled & {
            top: 16px;
        }
    }

    &__input {
        display: block;
        width: 100%;
        background: $color-5;
        border-radius: 8px;
        height: 80px;
        font-size: 20px;
        line-height: 24px;
        letter-spacing: -0.02em;
        color: $color-6;
        padding: 0 16px;

        .filled & {
            padding-top: 20px;
        }
    }
}
</style>
