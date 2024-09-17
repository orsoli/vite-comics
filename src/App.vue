<script>
// Import components 
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"


export default {
  data() {
    return {
      count: 0
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
  <div class="wrapper">
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  background-color: #0E0E0E;
  margin: -10px;
}
</style>
