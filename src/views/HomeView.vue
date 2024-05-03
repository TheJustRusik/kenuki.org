<template>
  <main class="max-w-screen-lg mx-auto">
    <div class="flex justify-between">
      <h2 class="tracking-widest uppercase text-3xl mb-4">Products</h2>
      <v-btn append-icon="mdi-arrow-right" variant="outlined" color="blue">
        See all products
      </v-btn>
    </div>
    
    
    <div class="sm:grid sm:grid-cols-2 md:grid-cols-3 gap-2 mb-4">
      <ProductPreviewCard title="Hi" subtitle="Sub" text="Some text lol kek text lol kek text lol kek text lol kek text lol kek" image="https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg"></ProductPreviewCard>      
      <ProductPreviewCard title="Hi" subtitle="Sub" text="Some text lol kek text lol kek text lol kek text lol kek text lol kek" image="https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg"></ProductPreviewCard>
      <ProductPreviewCard title="Hi" subtitle="Sub" text="Some text lol kek text lol kek text lol kek text lol kek text lol kek" image="https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg"></ProductPreviewCard>
    </div>

    <div class="flex justify-between">
      <h2 class="tracking-widest uppercase text-3xl mb-4">Projects</h2>
      <v-btn append-icon="mdi-arrow-right" variant="outlined" color="blue">
        See all projects
      </v-btn>
    </div>

  </main>
  
</template>

<script setup>
  import { ref } from "vue";
  import ProductPreviewCard from '../components/ProductPreviewCard.vue'
</script>