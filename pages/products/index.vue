<template>
  <div>
    <div class="grid grid-cols-1 gap-5 md:grid-cols-2 lg:grid-cols-4">
      <div v-for="p in products" v-bind:key="p.id">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
//  fetch the products
const { data: products } = await useFetch("https://fakestoreapi.com/products");
definePageMeta({
  layout: "products",
});
</script>
