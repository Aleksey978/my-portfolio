<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue";
export default {
  components: { Header, Main }
}

</script>
  

<template>
  <div>
    <Header></Header>
    <Main class="main"></Main>
  </div>
  
</template>

<style scoped>
.main {
  margin-top: 200px;
}
</style>
