<template>
    <form class="main-form">
        <div class="main-form__heading">Планируйте свою следующую поездку</div>
        <div class="main-form__fieldset">
            <ul>
                <li>
                    <main-form-text-field
                        icon="search"
                        label="Куда хотите поехать?"
                    ></main-form-text-field>
                </li>
                <li>
                    <main-form-text-field
                        icon="calendar"
                        label="Туда"
                        value="20.07.2020"
                    ></main-form-text-field>
                </li>
                <li>
                    <main-form-text-field
                        label="Обратно"
                        value="1.08.2020"
                    ></main-form-text-field>
                </li>
                <li>
                    <custom-button
                        text="Найти"
                        theme="primary"
                        type="submit"
                    ></custom-button>
                </li>
            </ul>
        </div>
        <div class="main-form__forecast">
            <ul>
                <li>
                    <div>Cейчас в Перми</div>
                    <div>
                        <ul>
                            <li>18:30, МСК+2</li>
                            <li>23˚ C, солнечно</li>
                        </ul>
                    </div>
                </li>
                <li>
                    <div>Завтра</div>
                    <div>21˚ C, облачно</div>
                </li>
                <li>
                    <div>29 июля</div>
                    <div>23˚ C, солнечно</div>
                </li>
                <li>
                    <div>30 июля</div>
                    <div>24˚ C, облачно</div>
                </li>
            </ul>
        </div>
        <div class="main-form__footer">
            <a
                href="#"
                class="main-form__more-link"
                title="Узнать больше о Пермском крае"
            >
                <i>
                    <svg
                        width="32"
                        height="32"
                        viewBox="0 0 32 32"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <title>Info</title>
                        <path
                            fill-rule="evenodd"
                            clip-rule="evenodd"
                            d="M16 27C22.0751 27 27 22.0751 27 16C27 9.92487 22.0751 5 16 5C9.92487 5 5 9.92487 5 16C5 22.0751 9.92487 27 16 27ZM16 30C23.732 30 30 23.732 30 16C30 8.26801 23.732 2 16 2C8.26801 2 2 8.26801 2 16C2 23.732 8.26801 30 16 30Z"
                            fill="white"
                        />
                        <path
                            d="M17.1468 11.072C17.9868 11.072 18.6168 10.442 18.6168 9.60196C18.6168 8.76196 17.9868 8.13196 17.1468 8.13196C16.3278 8.13196 15.6768 8.76196 15.6768 9.60196C15.6768 10.442 16.3278 11.072 17.1468 11.072ZM15.7398 23.21C17.0838 23.21 18.0708 22.034 18.8478 19.955L18.4698 19.829C17.9658 20.921 17.4828 21.341 17.0628 21.341C16.7268 21.341 16.6008 20.984 16.7268 20.354L17.9868 13.214H17.9238L13.5348 13.97V14.222L15.0048 14.915L14.0388 20.354C13.7028 22.202 14.3748 23.21 15.7398 23.21Z"
                            fill="white"
                        />
                    </svg>
                </i>
                <span>Узнать больше о Пермском крае</span>
            </a>
        </div>
    </form>
</template>

<script>
import MainFormTextField from "@/components/MainFormTextField";
import CustomButton from "@/components/CustomButton";

export default {
    components: {
        MainFormTextField,
        CustomButton,
    },
};
</script>

<style lang="scss">
.main-form {
    position: relative;
    z-index: 0;
    color: $color-5;
    background-image: url("~@/assets/images/main_form_background.png");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    border-radius: 24px;
    overflow: hidden;
    padding: 24px 16px;
    height: 100%;

    &::before {
        position: absolute;
        z-index: -1;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(#111111, 0.6);
        content: "";
    }

    &__heading {
        margin-bottom: 24px;
        font-size: 42px;
        line-height: 48px;
        letter-spacing: -0.02em;
    }

    &__fieldset {
        margin-bottom: 40px;

        li:not(:last-child) {
            margin-bottom: 16px;
        }
    }

    &__forecast {
        margin-bottom: 40px;

        > ul > li {
            display: flex;
            align-items: baseline;

            &:not(:last-child) {
                margin-bottom: 24px;
            }

            > div:first-child {
                flex: 0 0 150px;
                max-width: 150px;
                font-weight: bold;
                font-size: 20px;
                line-height: 24px;
                letter-spacing: -0.02em;
                margin-right: 30px;
            }

            > div:last-child {
                font-size: 20px;
                line-height: 24px;
                letter-spacing: -0.02em;
            }
        }

        ul ul li:not(:last-child) {
            margin-bottom: 8px;
        }
    }

    &__more-link {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 64px;
        border: 3px solid currentColor;
        border-radius: 64px;
        padding-right: 14px;

        i {
            position: absolute;
            left: 29px;
            top: calc(50% - 16px);

            svg {
                display: block;
            }
        }

        span {
            font-weight: 500;
            font-size: 28px;
            line-height: 32px;
            letter-spacing: -0.03em;
        }
    }
}
</style>
