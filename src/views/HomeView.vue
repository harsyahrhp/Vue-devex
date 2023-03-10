<script setup lang="ts">
import copy from '@/components/copy.vue';
</script>

<template>
  <body>
    <copy/>
  </body>
</template>

<style>
body{
  background-image: url('src/assets/Image/bck.webp');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  padding-bottom: 3rem;
}

.dx-datagrid {
    color: black;
    text-decoration: bold;
    background-color: rgba(255, 255, 255, 0.8);
    line-height: inherit;
    text-align: center;
}

.dx-datagrid-headers {
    color: black;
    font-weight: 4000;
}
</style>
