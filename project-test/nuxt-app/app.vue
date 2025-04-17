<template>
  <div class="root">
    <Header class="header" />
    <main class="body">
      <slot /> <!-- или <Nuxt /> для Nuxt 3 -->
    </main>
    <Footer class="footer" />
  </div>
</template>

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
  box-sizing: border-box; /* Рекомендуется добавить */
}
</style>


