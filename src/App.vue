<template>
  <div class="container">
    <Header/>
    <div class="row">
      <div class="col-xs-12">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Header
  },
  created() {
    this.$store.dispatch("initStocks");
  }
};
</script>


<style lang="scss">
body {
  padding: 30px;
}
</style>
