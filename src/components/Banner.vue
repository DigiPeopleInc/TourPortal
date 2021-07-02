<template>
    <div class="banner">
        <div class="banner__main">
            <div class="banner__section">
                <a
                    href="#"
                    title="Составь свой уникальный маршрут"
                    class="banner__btn"
                    >Составь</a
                >
            </div>
            <div class="banner__section">
                <div class="banner__text">свой уникальный маршрут</div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.banner {
    display: grid;
    align-items: center;
    width: 100%;
    height: 100%;
    background-image: url("~@/assets/images/banner_bg.png");
    background-repeat: no-repeat;
    background-position: top;
    background-size: 100% auto;
    background-color: $color-1;
    border-radius: 24px;
    color: $color-5;
    padding-bottom: 3px;

    &__section {
        display: flex;
        justify-content: center;
    }

    &__section:not(:last-child) {
        margin-bottom: 24px;
    }

    &__btn {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 256px;
        height: 80px;
        border-radius: 12px;
        background-color: $color-5;
        color: $color-1;
        font-size: 46px;
        line-height: 48px;
    }

    &__text {
        font-family: $font-2;
        font-style: italic;
        font-weight: 600;
        font-size: 46px;
        line-height: 56px;
        text-align: center;
    }
}
</style>
