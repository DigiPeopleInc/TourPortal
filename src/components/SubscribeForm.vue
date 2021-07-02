<template>
    <form class="subscribe-form">
        <div class="subscribe-form__grid">
            <div class="subscribe-form__cell">
                <div class="subscribe-form__heading">
                    Главные события Пермского края в еженедельной рассылке
                </div>
            </div>
            <div class="subscribe-form__cell">
                <subscribe-form-text-field
                    label="Ваша электронная почта"
                ></subscribe-form-text-field>
            </div>
            <div class="subscribe-form__cell">
                <custom-button
                    text="Подписаться"
                    theme="primary"
                    type="submit"
                ></custom-button>
            </div>
        </div>
    </form>
</template>

<script>
import SubscribeFormTextField from "@/components/SubscribeFormTextField";
import CustomButton from "@/components/CustomButton";

export default {
    components: {
        SubscribeFormTextField,
        CustomButton,
    },
};
</script>

<style lang="scss">
.subscribe-form {
    background-color: $color-3;
    border-radius: 24px;
    padding: 24px 24px 32px;
    color: $color-4;
    background-image: url("~@/assets/images/subscribe_background.png");
    background-repeat: no-repeat;
    background-position: 940px 50%;

    &__grid {
        display: inline-grid;
        grid-template-columns: 540px 263px;
        grid-gap: 16px;
    }

    &__cell {
        &:nth-child(2) {
            grid-column: 1;
        }
    }

    &__heading {
        font-size: 35px;
        line-height: 40px;
        letter-spacing: -0.02em;
        color: $color-4;
    }
}
</style>
