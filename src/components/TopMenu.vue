<template>

  <header class="max-w-screen-lg mx-auto">
    <div class="flex justify-between items-center my-4">
      <a href="/" class="transition ease-in-out hover:scale-110 duration-300">
        <h1 class="logo text-red-500 text-5xl">kenuki</h1>
        <h2 class="sublogo text-xs font-bold text-red-500 text-center">is TheJustRusik</h2>
      </a>
      <div class="flex items-center gap-6">
        <v-btn-toggle
          v-model="toggle"
          variant="text"
          color="red"
          divided
          mandatory
        >
          <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">Home</v-btn>
          <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">Projects</v-btn>
          <v-btn class="transition ease-in-out hover:-translate-y-1 duration-300">About</v-btn>
        </v-btn-toggle>

        <v-btn :icon="darkTheme ? 'mdi-white-balance-sunny' : 'mdi-weather-night'" @click="toggleTheme" ></v-btn>
      </div>
    
  </div>
  <v-divider class=" mb-4"></v-divider>
  </header>
  
</template>

<script setup>
import { useTheme } from 'vuetify'
import { ref } from "vue"


const theme = useTheme()

function toggleTheme () {
  darkTheme.value = !darkTheme.value;
  theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}

var toggle = ref(0)
var darkTheme = ref(false)//true = dark, false = light

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