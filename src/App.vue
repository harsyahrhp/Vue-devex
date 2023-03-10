<script setup lang="ts">
import Footer from './components/Footer.vue';
import Navbar from './components/Navbar.vue';
import HomeView from './views/HomeView.vue';

</script>

<template>
<Navbar/>
<body>
  <RouterView />  
</body>

<Footer/>
</template>

<style scoped>

</style>
