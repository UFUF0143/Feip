<template>
    <section class="block-info">
        <div class="block-info-title">
            Каждый проект для нас - важный
        </div>
        <div class="block-info-text">
            <p>
                Мы строительная компания полного цикла.
            </p>
            <p>
                Вникаем во все детали, разрабатываем планировку 
                будущего дома, продумываем конструктивные решения Add commentMore actions
                и общую архитектурную концепцию
            </p>
        </div>
        <div class="block-info-card">
            <img сlass ="card-info-icon" src="../public/image/house.svg" alt="">
            <div class="card-info-title">
                57 домов
            </div>
            <div class="card-info-subtitle">
                спроектировали и построили “под ключ”
            </div>
        </div>
        <div class="block-info-card">
            <img сlass ="card-info-icon" src="../public/image/calendar.svg" alt="">
            <div class="card-info-title">
                14 лет
            </div>
            <div class="card-info-subtitle">
                мы на рынке загородного строительства
            </div>
        </div>
    </section>
</template>

<style >
    .block-info{
        display: grid;
        grid-template-columns: 2fr 1fr 1fr;
        margin-bottom: 120px;
        column-gap: 16px;
    }
    .block-info-title{
        font-family: Monserrat, sans-serif;
        font-size: 38px;
        width: 50%;
        font-weight: 700;
        line-height: 120%;
        grid-column-start: 1;
        grid-column-end: 4;
    }

    .block-info-text{
        font-family: Open Sans, sans-serif;
        font-size: 20px;
        line-height: 135%;
        display: flex;
        justify-content: space-around;
        flex-direction: column;
        color: #666666;
    }

    .block-info-card{
        background-color: #F5F7F3;
        border-radius: 20px;
        padding: 24px;
    }
    .block-info-card img{
            margin-bottom: 24px;
        }

    .card-info-title{
        font-family: Monserrat, sans-serif;
        font-size: 24px;
        font-weight: 700;
        margin-bottom: 8px;
        line-height: 120%;
    }

    .card-info-subtitle{
        font-family: Open Sans, sans-serif;
        font-size: 20px;
        line-height: 135%;
    }

    @media(max-width: 824px){
        .block-info{
            grid-template-columns: 1fr;
            gap: 32px;
            background: white;
            margin-bottom: 80px;
        }

        .block-info-title{
            grid-column-start: 1;
            grid-column-end: 2;
            font-size: 28px;
            width: 100%;
        }

        .block-info-text{
            gap: 30px;
        }
    }
</style>