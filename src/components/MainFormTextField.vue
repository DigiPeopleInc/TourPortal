<template>
    <div :class="['main-text-field', { filled: value }]">
        <label class="main-text-field__label" :for="id">{{ label }}</label>
        <input
            type="text"
            class="main-text-field__input"
            :value="value"
            readonly
            :id="id"
        />
        <i :class="['main-text-field__icon', icon]" v-if="icon">
            <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                v-if="icon === 'search'"
            >
                <title>Lens</title>
                <circle
                    cx="10.125"
                    cy="10.125"
                    r="6.125"
                    stroke="white"
                    stroke-width="2"
                />
                <path
                    d="M17.625 16.125L23.25 21.75L21.75 23.25L16.125 17.625L17.625 16.125Z"
                    fill="white"
                />
            </svg>
            <svg
                width="33"
                height="32"
                viewBox="0 0 33 32"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                v-if="icon === 'calendar'"
            >
                <title>Calendar</title>
                <rect
                    x="4.85995"
                    y="14"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="4.85995"
                    y="21"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="18.9056"
                    y="14"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="18.9056"
                    y="21"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="18.9056"
                    y="7"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="11.8828"
                    y="14"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="11.8828"
                    y="21"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="11.8828"
                    y="7"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="25.9284"
                    y="14"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
                <rect
                    x="25.9284"
                    y="7"
                    width="4.01303"
                    height="4"
                    fill="white"
                />
            </svg>
        </i>
    </div>
</template>

<script>
export default {
    props: ["label", "value", "icon"],
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
.main-text-field {
    position: relative;

    &__label {
        position: absolute;
        top: calc(50% - 12px);
        font-size: 18px;
        line-height: 24px;
        letter-spacing: -0.02em;
        color: $color-5;
        pointer-events: none;
        padding: 0 16px;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;

        .filled & {
            font-weight: 500;
            top: 14px;
            font-size: 14px;
        }
    }

    &__icon {
        position: absolute;
        right: 16px;
        top: 50%;
        width: 32px;
        display: flex;
        justify-content: center;
        transform: translateY(-50%);

        svg {
            display: block;
        }

        &.search {
            margin-top: -5px;
            margin-right: 4px;
        }
    }

    &__input {
        display: block;
        width: 100%;
        background: rgba(245, 246, 247, 0.3);
        border-radius: 8px;
        height: 80px;
        font-size: 18px;
        line-height: 24px;
        letter-spacing: -0.02em;
        color: $color-5;
        padding: 0 16px;

        .filled & {
            padding-top: 23px;
        }
    }
}
</style>
