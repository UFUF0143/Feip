<template>
  <div class="projects">
    <h2 class="projects-title">Реализованные проекты</h2>
    <div class="projects__cards cards">
      <div v-for='project in projects' class="cards__elem">
        <div class="cards__text">
          <h3 id="header">{{project.title}}</h3>
          <p>{{project.description1}}</p>
          <p id="description2">{{project.description2}}</p>
        </div>
        <picture>
          <source :srcset='`${project.image.x2} 2x, ${project.image.x1}`'>
          <img :src='project.image.x1' :alt='project.title' class='image' />
        </picture>
      </div>
    </div>

  </div>
</template>
<script setup lang="ts">
  import scandinavian_house_1x from '../public/image/project-1-landscape.jpg';
  import scandinavian_house_2x from '../public/image/project-1-landscape@2x.jpg';
  import aerated_concrete_house_1x from '../public/image/project-2-landscape.jpg';
  import aerated_concrete_house_2x from '../public/image/project-2-landscape@2x.jpg';


  const projects = [
    {
      image: {
        x1: scandinavian_house_1x,
        x2: scandinavian_house_2x,
      },
      title: 'Дом в скандинавском стиле',
      description1: 'Одноэтажный дом из газобетона габаритными размерами 10.73 х 10.73 м.и ' +
          'жилой площадью 101 кв. м. с вальмовой кровлей',
      description2: 'Построен по индивидуальному проекту.'
    },

    {
      image: {
        x1: aerated_concrete_house_1x,
        x2: aerated_concrete_house_2x,
      },
      title: 'Дом из газобетона',
      description1: 'Одноэтажный дом габаритными размерами 15.2 х 9.7м. Приведенная площадь' +
          ' – 127.7 м.кв.',

      description2: 'Три спальные комнаты, два сан.узла, большая кухня-гостиная с выходом на террасу.'

    }
  ]
</script>

<style scoped>
  h2 {
    margin: 0;
  }

  .projects {
    display: flex;
    flex-direction: column;
    row-gap: 32px;
    padding-block: 80px;
    padding-inline: 92px;

  }
  .projects-title{
    font-family: Monserrat, sans-serif;
    font-size: 38px;
  }
  .const .projects{
    font-family: Monserrat, sans-serif;
    font-size: 38px;
  }
  .image {
    border-radius: 0px 20px 20px 0px;
  }

  .cards__elem {
    display: flex;
    border-radius: 20px;
    background: white;
    max-width: 624px;
  }

  .projects__cards {
    display: grid;
    display: flex;
    column-gap: 16px;
    grid-template-columns: 1fr 1fr;
    justify-content: space-between;
  }

  .cards__text {
    margin: 32px 16px 16px 32px;
  }
  .cards__text h3{
    font-family: Monserrat, sans-serif;
    font-size: 20px;
    line-height: 120%;
  }
  .cards__text p{
    font-family: Open Sans, sans-serif;
    font-size: 16px;
    line-height: 135%;
  }

  img {
    width: 304px;
    object-fit: cover;
    height: 100%;
  }

  .cards__elem #header {
    padding-bottom: 12px;
  }
    #description2 {
    margin-top: 16px;
  }

  .projects__cards::-webkit-scrollbar {
    width: 0;
    height: 0;
  }

  .projects__cards {
    scrollbar-width: none;
  }

  @media (max-width: 1350px) {

    img {
      max-width: 400px;
      width: 100%;
      min-width: 304px;
      ;
    }

    .cards__elem {
      flex-direction: column;
      max-width: 400px;

    }

    .cards__text {
      order: 2;
    }

    picture {
      order: 1;
    }

    .image {
      border-radius: 20px 20px 0px 0px;
    }
  }

  @media (max-width: 1060px) {
    .projects{
        padding-inline: 16px;
    }
    .cards__elem {
      height: 453px;
    }

    .cards__text {
      margin: 21px 24.5px 24px 24.5px;
    }

    .image {
      height: 150px;
    }

    .projects {
      row-gap: 23px;
    }

    .cards__elem #header {
      padding-bottom: 12px;
    }

    .projects__cards {
      overflow-x: auto;
    }
  }
</style>