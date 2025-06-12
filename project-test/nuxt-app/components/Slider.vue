<template>
    <Swiper :modules="modules"
    navigation pagination :loop="true">
      <SwiperSlide v-for="slide in slides">
        <figure class="slider-figure">
          <picture class="slider-figure-picture">
            <source
              :srcset="`${slide.image_landscape.x2} 2x, ${slide.image_landscape.x1}`"
              media="(min-width: 768px)"
            >
            <source :srcset="`${slide.image_portrait.x2} 2x, ${slide.image_portrait.x1}`">
                    <img :src="slide.image_portrait.x1" :alt='slide.title'>
          </picture>
          <figcaption class="slider-figure-caption">
            <p class="caption-title">{{ slide.title }}</p>
            <p class="caption-text">{{ slide.text }}</p>
          </figcaption>
        </figure>
      </SwiperSlide>
    </Swiper>
</template>
<script setup>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import { Navigation, Pagination } from 'swiper/modules';
    import 'swiper/css';
    import 'swiper/css/navigation';
    import 'swiper/css/pagination';
    import slide1_portrait_1x from '../public/image/slide-1-portrait.jpg'
    import slide1_portrait_2x from '../public/image/slide-1-portrait@2x.jpg'
    import slide1_landscape_1x from '../public/image/slide-1-landscape.jpg'
    import slide1_landscape_2x from '../public/image/slide-1-landscape@2x.jpg'
    import slide2_portrait_1x from '../public/image/slide-2-portrait.jpg'
    import slide2_portrait_2x from '../public/image/slide-2-portrait@2x.jpg'
    import slide2_landscape_1x from '../public/image/slide-2-landscape.jpg'
    import slide2_landscape_2x from '../public/image/slide-2-landscape@2x.jpg'
    import slide3_portrait_1x from '../public/image/slide-3-portrait.jpg'
    import slide3_portrait_2x from '../public/image/slide-3-portrait@2x.jpg'
    import slide3_landscape_1x from '../public/image/slide-3-landscape.jpg'
    import slide3_landscape_2x from '../public/image/slide-3-landscape@2x.jpg'
    
    const modules = [Navigation, Pagination];
    
    const slides = [
        {
        image_portrait: {
            x1: slide1_portrait_1x,
            x2: slide1_portrait_2x
        },
        image_landscape: {
            x1: slide1_landscape_1x,
            x2: slide1_landscape_2x
        },
        title: 'Проектируем и строим загородные дома',
        text: 'Строим дома «под ключ»: от этапа проектирования и до финишной отделки помещений'
        },
        {
        image_portrait: {
            x1: slide2_portrait_1x,
            x2: slide2_portrait_2x
        },
        image_landscape: {
            x1: slide2_landscape_1x,
            x2: slide2_landscape_2x
        },
        title: 'Материалы и технологии',
        text: 'Используем проверенные строительные решения и экологичные материалы, чтобы ваш дом был прочным, теплым и долговечным'
        },
        {
        image_portrait: {
            x1: slide3_portrait_1x,
            x2: slide3_portrait_2x
        },
        image_landscape: {
            x1: slide3_landscape_1x,
            x2: slide3_landscape_2x
        },
        title: 'Индивидуальный подход к каждому клиенту',
        text: 'Создаем дома по вашим эскизам или предлагаем готовые проекты с возможностью адаптации под ваши пожелания'
        },
    ];
</script>
<style lang="scss">
    .body{
        padding: 0 88px;
    }
    .swiper{
        width: 100%;
        border-radius: 30px;
        margin-bottom: 120px;
        margin-top: 40px;
        
    }

    .slider-figure {
    position: relative;
    }

    .slider-figure img {
        height: 450px;
        max-width: 100%;
        width: 100%;
        object-fit: cover;
    }

    .slider-figure-picture {
        position: relative;
    }

    .slider-figure::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 450px;
        z-index: 5;
        background: linear-gradient(
            to right,
            rgba(0, 0, 0, 0.8) 0%,
            rgba(0, 0, 0, 0) 100%
        );
    }

    .slider-figure-caption {
        position: absolute;
        bottom: 113px;
        left: 144px;
        right: 144px;
        color: white;
        z-index: 10;
        display: flex;
        flex-direction: column;
        gap: 12px;
        max-width: 460px;
    }

    .caption-title{
        font-family: Monserrat, sans-serif;
        font-weight: 700;
        font-size: 46px;
        line-height: 120%;
    }

    .caption-text{
        font-family: Open Sans, sans-serif;
        font-size: 16px;
        line-height: 135%;
    }

    .swiper-pagination {
    margin-bottom: 40px;
    }

    .swiper-pagination-bullet {
    background-color: #C6C6C6;
    opacity: 1;
    margin: 0 12px;
    }

    .swiper-pagination-bullet-active {
    background-color: #03B766;
    }

    .swiper-button-next, .swiper-button-prev{
        background-color: #03B766;
        color: white;
        padding: 2px 22px;
        border-radius: 10px;;
    }

    .swiper-button-prev:after, .swiper-button-next:after{
        font-size: 12px;
    }

    @media(max-width: 825px){
        .caption-title{
            font-size: 30px;
        }

        .caption-text{
            font-size: 16px;
        }
        .swiper{
            margin-top: 24px;
            margin-bottom: 80px;
        }

        .swiper-pagination{
            display: none;
        }
        .swiper-button-next, .swiper-button-prev{
            display: none;
        }
        .slider-figure-caption {
             bottom: 30px;
             left: 24px;
             right: 24px;
        }

    }
</style>
