<template>

  <header class="max-w-screen-lg mx-auto">
    <div class="flex justify-between items-center my-4">
    <a href="/" class="transition ease-in-out hover:scale-110 duration-300">
      <h1 class="logo text-red-500 text-5xl">kenuki</h1>
      <h2 class="sublogo text-xs font-bold text-red-500 text-center">is TheJustRusik</h2>
    </a>

    <v-btn-toggle
      v-model="toggle"
      variant="text"
      color="red"
      divided
    >
      <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">Products</v-btn>
      <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">Projects</v-btn>
      <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">Comments</v-btn>
      <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">About</v-btn>
    </v-btn-toggle>

    
  </div>
  <v-divider class="border-opacity-100 mb-4"></v-divider>
  </header>
  
</template>

<script setup>
import { ref } from "vue"

var toggle = ref()

</script>

<style>
  @font-face {
    font-family: 'Dimis';
    src: url('/src/assets/DIMIS___.TTF') format('truetype');
  }
  @font-face {
    font-family: 'Montserrat';
    src: url('/src/assets/Montserrat-VariableFont_wght.ttf') format('truetype');
  }

  .logo {
    font-family: 'Dimis', sans-serif;
  }
  .sublogo {
    font-family: 'Montserrat', sans-serif;
  }

</style>