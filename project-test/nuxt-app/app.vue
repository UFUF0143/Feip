<template>
  <div class="root">
    <Header class="header" />
    <main class="body">
        <div class="main__container _container">
            <Slider />
            <BlockInfo />
        </div>
    </main>
    <Footer class="footer" />
  </div>
</template>
<script>
    import BlockInfo from './components/BlockInfo.vue';
import Slider from './components/Slider.vue'
</script>

<style scoped>

.root {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.header, .footer { 
  flex-shrink: 0;
}
.body {
  flex-grow: 1;
}
</style>

<style>
/* Глобальные стили лучше вынести в отдельный тег без scoped */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
}
</style>


