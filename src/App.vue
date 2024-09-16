<script>
// Import components 
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"


export default {
  data() {
    return {
      count: 0
    }
  },
  components: {
    AppHeader,
    AppMain,
  }
}
</script>

<template>
  <div class="wrapper">
    <AppHeader />
    <AppMain />

  </div>
</template>

<style scoped>
.wrapper {
  padding: 20px 0;
  background-color: #0E0E0E;
}
</style>
