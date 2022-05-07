<template>
  <div id="app">
    <header-component :title="titolo" />
    <main>
      <main-grid />
    </main>
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainGrid from './components/MainGrid.vue'


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainGrid,
    
  },
  data() {
    return {
      titolo: "rick & morty",
    }
  }
}



</script>

<style lang="scss">
@import "./style/generals.scss"
// @import "@/assets/style/generals.scss";    
// la @ parte sempre dalla cartella src



</style>
