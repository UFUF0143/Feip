<template>
  <div class="root">
    <Header class="header" />
    <main class="body">
        <div class="main-container">
            <Slider class="slider" />
            <BlockInfo class="blockinfo" />
        </div>
        <div class="projects">
          <Project class="project" />
          <News class="news" />
        </div>
    </main>
    <Footer class="footer" />
  </div>
</template>
<script>
import BlockInfo from './components/BlockInfo.vue';
import News from './components/News.vue';
import Project from './components/Project.vue';
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
.main-container{
  padding: 0 88px;
}
.body {
  flex-grow: 1;
}
@media(max-width: 1060px){
  .main-container{
  padding: 0 16px;
}
}
</style>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
}
.project{
  background-color: rgba(245, 247, 243, 1);
  padding: 80px 88px;

}

</style>


