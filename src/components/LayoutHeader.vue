<template>
    <header class="header">
        <div class="header__section">
            <container>
                <div class="header__row">
                    <div class="header__cell">
                        <nav class="header__contact-menu">
                            <ul>
                                <li>
                                    <button type="button">
                                        Туристские информационные центры
                                    </button>
                                </li>
                                <li>
                                    <a
                                        href="tel:+73422141080"
                                        title="+73422141080"
                                        >+7 (342) 214 10 80</a
                                    >
                                </li>
                                <li>
                                    ул. Ленина, 39
                                </li>
                            </ul>
                        </nav>
                    </div>
                    <div class="header__cell">
                        <nav class="header__secondary-menu">
                            <ul>
                                <li>
                                    <a href="#" title="Английския язык">
                                        <svg
                                            width="21"
                                            height="11"
                                            viewBox="0 0 21 11"
                                            fill="none"
                                            xmlns="http://www.w3.org/2000/svg"
                                        >
                                            <title>EN</title>
                                            <path
                                                d="M0.5 0V11H8.69925V9.03572H2.56511V6.31714H8.08736V4.35286H2.56511V1.96429H8.54627V0H0.5Z"
                                                fill="white"
                                            />
                                            <path
                                                d="M12.4843 1.46143L16.9358 11H20.5V0H18.4349V9.53857L13.9834 0H10.4192V11H12.4843V1.46143Z"
                                                fill="white"
                                            />
                                        </svg>
                                    </a>
                                </li>
                                <li>
                                    <a href="#" title="Версия для слабовидящих">
                                        <svg
                                            width="25"
                                            height="15"
                                            viewBox="0 0 25 15"
                                            fill="none"
                                            xmlns="http://www.w3.org/2000/svg"
                                        >
                                            <title>Glasses</title>
                                            <path
                                                fill-rule="evenodd"
                                                clip-rule="evenodd"
                                                d="M0.500001 1C0.500001 0.5 0.982233 0 1.5 0H4.5C4.5 0 4.5 0.447715 4.5 1C4.5 1.55228 4.5 2 4.5 2H2.5V6.99951C3.41223 5.78534 4.8644 5 6.5 5C8.07222 5 9.47495 5.72566 10.3915 6.86031C10.9334 6.24608 11.6781 6 12.5 6C13.3219 6 14.0666 6.24608 14.6085 6.86031C15.5251 5.72566 16.9278 5 18.5 5C20.1356 5 21.5878 5.78534 22.5 6.99951V2H20.5C20.5 2 20.5 1.55228 20.5 1C20.5 0.447715 20.5 0 20.5 0H23.5C24.0523 0 24.5 0.447715 24.5 1V9C24.5 9.55229 24.0523 10 23.5 10C23.5 12.7614 21.2614 15 18.5 15C15.7386 15 13.5 12.7614 13.5 10C13.5 8.5 13 8 12.5 8C12 8 11.5 8.5 11.5 10C11.5 12.7614 9.26142 15 6.5 15C3.73858 15 1.5 12.7614 1.5 10C0.947715 10 0.5 9.55229 0.5 9L0.500001 1ZM6.5 13C8.15685 13 9.5 11.6569 9.5 10C9.5 8.34315 8.15685 7 6.5 7C4.84315 7 3.5 8.34315 3.5 10C3.5 11.6569 4.84315 13 6.5 13ZM15.5 10C15.5 11.6569 16.8431 13 18.5 13C20.1569 13 21.5 11.6569 21.5 10C21.5 8.34315 20.1569 7 18.5 7C16.8431 7 15.5 8.34315 15.5 10Z"
                                                fill="white"
                                            />
                                        </svg>
                                    </a>
                                </li>
                                <li>
                                    <a href="#" title="Карта"
                                        ><span>Карта</span></a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Маршрут"
                                        ><span>Маршрут</span></a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Избранное"
                                        ><span>Избранное</span><i>4</i></a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Войти"
                                        ><span>Войти</span></a
                                    >
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </container>
        </div>
        <div class="header__section">
            <container>
                <div class="header__row header__row--second">
                    <div class="header__cell">
                        <a href="/" title="На Главную">
                            <img
                                src="@/assets/images/logo.png"
                                alt="Туристический портал пермского края"
                            />
                        </a>
                    </div>
                    <div class="header__cell">
                        <nav class="header__main-menu">
                            <ul>
                                <li>
                                    <a href="#" title="О крае">О крае</a>
                                </li>
                                <li>
                                    <a href="#" title="Чем заняться"
                                        >Чем заняться</a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Где остановиться"
                                        >Где остановиться</a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Как добраться"
                                        >Как добраться</a
                                    >
                                </li>
                                <li>
                                    <a href="#" title="Полезно">Полезно</a>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </container>
        </div>
    </header>
</template>

<script>
import Container from "@/components/Container";

export default {
    components: {
        Container,
    },
};
</script>

<style lang="scss">
.header {
    position: relative;
    z-index: 0;
    padding: 14px 0 24px;
    margin-bottom: 25px;
    background: linear-gradient(90.79deg, $color-2 34%, $color-1 94.98%);
    color: $color-5;

    &::after {
        position: absolute;
        z-index: -1;
        top: 100%;
        left: 0;
        width: 100%;
        height: 416px;
        background: linear-gradient(90.79deg, $color-2 34%, $color-1 94.98%);
        content: "";
    }

    &__section:not(:last-child) {
        margin-bottom: 36px;
    }

    &__row {
        display: flex;
        align-items: center;

        &--second {
            align-items: center;
        }
    }

    &__cell:last-child {
        margin-left: auto;
    }

    &__contact-menu {
        font-size: 18px;
        line-height: 24px;
        letter-spacing: -0.02em;

        button {
            border-bottom: 1px solid rgba($color-5, 0.3);
            letter-spacing: -0.02em;
        }

        ul {
            display: flex;

            li:not(:last-child) {
                margin-right: 27px;
            }
        }
    }

    &__secondary-menu {
        margin-right: 6px;
        margin-top: 6px;

        i {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 24px;
            height: 24px;
            background: $color-5;
            border-radius: 24px;
            color: $color-1;
            font-style: normal;
            font-size: 14px;
            line-height: 16px;
            margin-left: 8px;
        }

        span {
            font-size: 18px;
            line-height: 24px;
            letter-spacing: -0.02em;
        }

        a {
            display: flex;
        }

        ul {
            display: flex;
            align-items: baseline;

            li:not(:last-child) {
                margin-right: 33px;
            }
        }
    }

    &__main-menu {
        font-size: 24px;
        line-height: 32px;
        letter-spacing: -0.02em;

        ul {
            display: flex;
            align-items: baseline;

            li:not(:last-child) {
                margin-right: 33px;
            }
        }
    }
}
</style>
