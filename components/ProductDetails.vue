<template>
  <div class="card">
    <div class="grid grid-cols-1 gap-10 md:grid-cols-2 lg:grid-cols-2">
      <div class="p-7">
        <img :src="product.image" alt="Product" class="mx-auto my-7" />
      </div>
      <div class="p-7">
        <h2 class="text-4x1 my-7">{{ product.title }}</h2>
        <p class="text-xl my-7">Price -${{ product.price }}</p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">Product Desciption:</h3>
        <p class="mb-7">{{ product.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped>
img {
  max-width: 80%;
}
</style>
