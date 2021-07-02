<template>
    <section class="category-section">
        <container>
            <div class="category-section__header">
                <section-heading>Чем заняться</section-heading>
            </div>
            <div class="category-section__main">
                <category-list
                    :list="[
                        {
                            img: 'assets/categories/category_pic_1.png',
                            name: 'Активный отдых',
                        },
                        {
                            img: 'assets/categories/category_pic_2.png',
                            name: 'С детьми',
                        },
                        {
                            img: 'assets/categories/category_pic_3.png',
                            name: 'Круизы',
                        },
                        {
                            img: 'assets/categories/category_pic_4.png',
                            name: 'Еда',
                        },
                        {
                            img: 'assets/categories/category_pic_5.png',
                            name: 'Санатории',
                        },
                        {
                            img: 'assets/categories/category_pic_6.png',
                            name: 'Искусство',
                        },
                        {
                            img: 'assets/categories/category_pic_7.png',
                            name: 'История',
                        },
                    ]"
                ></category-list>
            </div>
            <div class="category-section__footer">
                <more-list
                    label="Другие активности и виды отдыха"
                    :list="[
                        'Спорт',
                        'Экскурсии и квесты',
                        'Достопримечательности',
                        'Выставки',
                        'Образование',
                        'Парки и скверы',
                        'Храмы',
                        'Памятники и скульптуры',
                        'Фестивали',
                        'Чудеса природы',
                        'Архитектура',
                    ]"
                ></more-list>
            </div>
        </container>
    </section>
</template>

<script>
import Container from "@/components/Container";
import SectionHeading from "@/components/SectionHeading";
import CategoryList from "@/components/CategoryList";
import MoreList from "@/components/MoreList";

export default {
    components: {
        Container,
        SectionHeading,
        CategoryList,
        MoreList,
    },
};
</script>

<style lang="scss">
.category-section {
    margin-bottom: 39px;

    &__header {
        margin-bottom: 40px;
    }

    &__main {
        margin-bottom: 40px;
    }
}
</style>
