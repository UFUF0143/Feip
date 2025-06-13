<template>
    <div class="news">
        <div class="news-header">
            <div class="news-header-title">
                Новости
            </div>
            <button class="news-header-button">
                Все новости
            </button>
        </div>
        <div class="news-cards">
            <NewsCard v-for="card in news" 
            :title='card.title'
            :text='card.text'
            :image='card.image'
            :date='card.date'/>
        </div>
    </div>
</template>

<script setup>
    import NewsCard from '../components/CardNews.vue'
    import news1_1x from '../public/image/room.jpg'
    import news1_2x from '../public/image/room@2x.jpg'
    import news2_1x from '../public/image/girl.jpg'
    import news2_2x from '../public/image/girl@2x.jpg'
    import news3_1x from '../public/image/tractor.jpg'
    import news3_2x from '../public/image/tractor@2x.jpg'
    import news4_1x from '../public/image/worker.jpg'
    import news4_2x from '../public/image/worker@2x.jpg'

    const news = [
        {
            image:{
                x1: news1_1x,
                x2: news1_2x,
            },
            date: '20 авг 2021',
            title: 'Как сделать строительство дешевле?',
            text: 'Строительство дома можно сделать дешевле — выбрав проект...'
        },
        {
            image:{
                x1: news2_1x,
                x2: news2_2x,
            },
            date: '20 авг 2021',
            title: 'Почему Гуд Вилл строит лучшие дома?',
            text: 'Хотим обрадовать тех, кто планирует переезд из квартиры в дом...'
        },
        {
            image:{
                x1: news3_1x,
                x2: news3_2x,
            },
            date: '20 авг 2021',
            title: 'Преимущества и недостатки частного дома',
            text: 'Первое и главное: строим дом индивидуально для вас, по вашим...'
        },
        {
            image:{
                x1: news4_1x,
                x2: news4_2x,
            },
            date: '20 авг 2021',
            title: 'Из чего мы строим дома в ипотеку?',
            text: 'Самый популярный вопрос наших клиентов касается материалов, которы...'
        },
    ]
</script>

<style scoped lang="scss">
    .news {
        padding-top: 80px;
        padding-bottom: 60px;
        padding-inline: 88px;
    }

    .news-header-title {
        font-family: Monserrat, sans-serif;
        font-weight: 700;
        font-size: 46px;
        line-height: 120%;
        
    }

    .news-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 32px;
    }

    .news-header-button {
        font-size: 14px;
        font-weight: 600;
        border-radius: 10px;
        padding: 16px 24px;
        color: #029F59;
        border: #029F59 solid 1px;
        background-color: #ffffff;
        font-family: Monserrat, sans-serif;
    }

    .news-cards{
        grid-template-columns: 1fr 1fr 1fr 1fr;
        scrollbar-width: none;
        display: grid;
        
        overflow: auto;
        column-gap: 16px;
    }

    @media(max-width: 1060px){
        .news{
            padding-top: 60px;
            padding-inline: 16px;
        }
    }
</style>

