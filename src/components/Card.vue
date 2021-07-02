<template>
    <div class="card">
        <div class="card__pic" :style="`background-image: url(${img})`">
            <div class="card__tools">
                <ul>
                    <li v-if="plus !== undefined">
                        <button
                            type="button"
                            class="card__btn"
                            title="Добавить"
                        >
                            <i>
                                <svg
                                    width="24"
                                    height="24"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    xmlns="http://www.w3.org/2000/svg"
                                >
                                    <title>Добавить</title>
                                    <path
                                        d="M11 5.5L13 5.5V18.5H11V5.5Z"
                                        fill="#111111"
                                    />
                                    <path
                                        d="M5.5 13V11H18.5V13H5.5Z"
                                        fill="#111111"
                                    />
                                </svg>
                            </i>
                        </button>
                    </li>
                    <li v-if="fav !== undefined">
                        <button
                            type="button"
                            class="card__btn"
                            title="В Избранное"
                            v-if="!fav"
                        >
                            <i
                                ><svg
                                    width="24"
                                    height="24"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    xmlns="http://www.w3.org/2000/svg"
                                >
                                    <title>В Избранное</title>
                                    <path
                                        d="M16.1479 4.89474C18.4689 4.89474 19.3026 6.78947 19.3026 8.50421C19.3026 11.4884 15.1342 16.0832 11.7237 18.6695C8.31316 16.0642 4.14474 11.5263 4.14474 8.50421C4.14474 6.78947 4.97842 4.89474 7.29947 4.89474C7.89057 4.94472 8.46169 5.13277 8.96684 5.44376C9.472 5.75475 9.89709 6.18 10.2079 6.68526L11.7237 8.68421L13.2395 6.67579C13.5514 6.17228 13.9769 5.74889 14.482 5.43959C14.9871 5.13028 15.5576 4.94367 16.1479 4.89474ZM16.1479 3C15.2607 3.04132 14.3962 3.29418 13.6266 3.73749C12.857 4.1808 12.2046 4.80171 11.7237 5.54842C11.2428 4.80171 10.5903 4.1808 9.82074 3.73749C9.05113 3.29418 8.18667 3.04132 7.29947 3C4.14474 3 2.25 5.46316 2.25 8.50421C2.25 13.0042 8.37 18.7547 11.7237 21C15.0774 18.7547 21.1974 13.0042 21.1974 8.50421C21.1974 5.46316 19.3026 3 16.1479 3Z"
                                        fill="#111111"
                                    />
                                </svg>
                            </i>
                        </button>
                        <button
                            type="button"
                            class="card__btn"
                            title="Убрать из Избранного"
                            v-if="fav"
                        >
                            <i>
                                <svg
                                    width="24"
                                    height="24"
                                    viewBox="0 0 24 24"
                                    fill="none"
                                    xmlns="http://www.w3.org/2000/svg"
                                >
                                    <title>Убрать из Избранного</title>
                                    <path
                                        d="M16.1479 3C15.2607 3.04132 14.3962 3.29418 13.6266 3.73749C12.857 4.1808 12.2046 4.80171 11.7237 5.54842C11.2428 4.80171 10.5903 4.1808 9.82074 3.73749C9.05113 3.29418 8.18667 3.04132 7.29947 3C4.14474 3 2.25 5.46316 2.25 8.50421C2.25 13.0042 8.37 18.7547 11.7237 21C15.0774 18.7547 21.1974 13.0042 21.1974 8.50421C21.1974 5.46316 19.3026 3 16.1479 3Z"
                                        fill="#F44E1F"
                                    />
                                </svg>
                            </i>
                        </button>
                    </li>
                </ul>
            </div>
        </div>
        <div class="card__main">
            <div class="card__tags">
                <ul>
                    <li v-for="(tag, index) in tags" :key="`tag-${index}`">
                        <a href="#" :title="tag" class="card__tag">{{ tag }}</a>
                    </li>
                </ul>
            </div>
            <div class="card__title">
                <a href="#" :title="title">{{ title }}</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ["img", "tags", "title", "fav", "plus"],
};
</script>

<style lang="scss">
.card {
    border-radius: 24px;
    overflow: hidden;
    background-color: $color-5;
    color: $color-4;

    &__pic {
        position: relative;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        height: 472px;
    }

    &__tools {
        position: absolute;
        right: 16px;
        bottom: 16px;

        ul {
            display: flex;

            li:not(:last-child) {
                margin-right: 8px;
            }
        }
    }

    &__main {
        padding: 16px;
        height: 184px;
    }

    &__tags {
        margin-bottom: 10px;
        max-height: 56px;
        overflow: hidden;

        ul {
            display: flex;
            flex-wrap: wrap;
            margin: -4px;

            li {
                padding: 4px;
            }
        }
    }

    &__tag {
        display: flex;
        align-items: center;
        padding: 0 7px;
        height: 20px;
        font-weight: 500;
        font-size: 12px;
        line-height: 16px;
        border: 1px solid currentColor;
        border-radius: 24px;
        text-transform: uppercase;
    }

    &__title {
        font-size: 30px;
        line-height: 32px;
        letter-spacing: -0.02em;
        max-height: (32px * 3);
        overflow: hidden;
    }

    &__btn {
        width: 32px;
        height: 32px;
        border-radius: 50%;
        background-color: $color-5;
        text-align: center;

        i {
            display: inline-block;
            vertical-align: middle;

            svg {
                display: block;
            }
        }
    }
}
</style>
