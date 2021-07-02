<template>
    <section class="main-section">
        <container>
            <div class="main-section__grid">
                <div class="main-section__cell">
                    <main-form></main-form>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_1.png"
                        :tags="['Пермь', '1 ДЕНЬ', '3 ТОЧКИ', '221 КМ']"
                        title="Пермский край за один день"
                        :fav="false"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_2.png"
                        :tags="['Кунгур', '~3 часа', 'бесплатно']"
                        title="Белогорский Свято-Николаевский монастырь"
                        :plus="false"
                        :fav="false"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_3.png"
                        :tags="['Чусовой', 'от 1500₽']"
                        title="Природный парк «Пермский»"
                        :plus="false"
                        :fav="false"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_4.png"
                        :tags="['Кунгур', '20 июня', '5000₽']"
                        title="Фестиваль воздухоплавания «Небесная ярмарка»"
                        :fav="false"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_5.png"
                        :tags="['Пермь', '14 ноября', '~45 мин', 'Бесплатно']"
                        title="Экскурсия в Хохловку"
                        :fav="true"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_6.png"
                        :tags="['4, 9, 14 ноября', '7 ТОЧек', 'от 500₽']"
                        title="Исторические города за три дня"
                        :fav="false"
                    ></card>
                </div>
                <div class="main-section__cell">
                    <banner></banner>
                </div>
                <div class="main-section__cell">
                    <card
                        img="assets/cards/card_pic_7.png"
                        :tags="['Губаха', 'Бесплатно']"
                        title="Ладейный Лог"
                        :plus="false"
                        :fav="false"
                    ></card>
                </div>
            </div>
            <div class="main-section__footer">
                <more-list
                    label="Еще идеи для отдыха"
                    :list="[
                        'Экскурсия в Каменный город',
                        'Катание на горнолыжных склонах Губахи',
                        'Кунгур: Ледяная пещера',
                        'Отдых в яхт-клубе «Волна»',
                        'Лечение в пантоцентре «Оленья застава»',
                        'Ручной круиз на теплоходе «Пермь»',
                        'Экскурсия на камень Ветлан',
                    ]"
                ></more-list>
            </div>
        </container>
    </section>
</template>

<script>
import Container from "@/components/Container";
import MainForm from "@/components/MainForm";
import Card from "@/components/Card";
import Banner from "@/components/Banner";
import MoreList from "@/components/MoreList";

export default {
    components: {
        Container,
        MainForm,
        Card,
        Banner,
        MoreList,
    },
};
</script>

<style lang="scss">
.main-section {
    position: relative;
    margin-bottom: 38px;

    &__grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-gap: 16px;
        margin-bottom: 16px;
    }

    &__cell:first-child {
        grid-column: 1 / 3;
        grid-row: 1 / span 2;
    }
}
</style>
