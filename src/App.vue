<script>
// Import components 
import AppHeader from "./components/AppHeader.vue"


export default {
  data() {
    return {
      count: 0
    }
  },
  components: {
    AppHeader,
  }
}
</script>

<template>
  <div class="wrapper">
    <AppHeader />

  </div>
</template>

<style scoped>
.wrapper {
  padding: 20px 0;
  background-color: #0E0E0E;
}
</style>
