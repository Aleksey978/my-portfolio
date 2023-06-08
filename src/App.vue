<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue";
export default {
  components: { Header, Main },
  data() {
    return {
      numberOfLines: 5, // Количество линий, которые вы хотите отобразить
      lineInterval: 16.9, // Интервал между каждой линией в пикселях
    };
  },
}

</script>
  

<template>
  <div class="container">
    <!-- <div v-for="index in numberOfLines" :key="index" class="line" :style="{ left: ((index - 1) * lineInterval) + 7 + '%' }"></div> -->
    <Header></Header>
    <Main class="main"></Main>
  </div>
  
</template>

<style scoped>
.main {
  margin-top: 126px;
}
@media (max-width: 1800px) {
    .main {
    margin-top: 70px;
}
}
.container {
  max-width: 1886px;
  margin-left: auto;
  margin-right: auto;
}
@media (max-width: 1980px) {
  .container {
  max-width: 1560px;
  }
}

@media (max-width: 1800px) {
  .container {
  max-width: 920px;
  }
}

@media (max-width: 1060px) {
  .container {
  max-width: 620px;
  }
}

@media (max-width: 704px) {
  .container {
  max-width: 320px;
  }
}

</style>
