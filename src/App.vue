<script setup>
  import Navbar from './components/Navbar.vue'
  import FooterView from './components/FooterView.vue';

  import { RouterView } from 'vue-router';

</script>

<template>
  <div class="container mx-auto px-5">
    
    <Navbar/>
      <RouterView/>
    <FooterView/>

  </div>
</template>

<style scoped>
</style>
