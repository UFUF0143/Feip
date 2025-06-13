<template>
    <div class="news-card">
        <picture class="news-card-picture">
            <source
            :srcset="`${image.x2} 2x, ${image.x1}`"
            >
            <img :src="image.x1" >
        </picture>
        <div class="news-card-info">
            <p class="news-card-date">{{date}}</p>
            <p class="news-card-title">{{title}}</p>
            <p class="news-card-text">{{text}}</p>
        </div>
    </div>
</template>

<script setup>
    defineProps({
        image: {
            x1: String,
            x2: String,
        },
        date: String,
        title: String,
        text: String,
    })
</script>

<style scoped lang="scss">
    .news-card {
        border-top-left-radius: 20px;
        border-top-right-radius: 20px;
        overflow: hidden;
        min-width: 304px;
    }

    .news-card-date {
        margin: 16px 0;
        font-family: Monserrat, sans-serif;
        font-size: 14px;
        font-weight: 400;
        line-height: 120%;
    }


    .news-card-text {
        font-family: Open Sans, sans-serif;
        font-size: 16px;
        font-weight: 400;
        line-height: 120%;
        color: #666666;
    }
    .news-card-title {
        margin-bottom: 8px;
        font-family: Monserrat, sans-serif;
        font-size: 20px;
        font-weight: 700;
        line-height: 120%;
    }

    .news-card-picture img {
        width: 100%;
        height: auto;
    }

    @media(max-width: 824px){
        .news-card{
            min-width: 344px;
        }
    }
</style>