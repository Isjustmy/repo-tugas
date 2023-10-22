<script setup lang="ts">
const props = defineProps({
  product: {
    type: Object,
    default: {},
  },
});
</script>

<template>
  <section class="py-10">
    <div class="container">
      <NuxtLink
        to="/product"
        class="bg-white border border-slate-300 w-max flex items-center gap-1 py-2 px-5 rounded-full mb-7 cursor-pointer ml-10"
      >
        <i class="ri-arrow-left-s-line text-base font-medium"></i>
        <span class="text-base font-medium">Kembali</span>
      </NuxtLink>
      <div class="flex items-center">
        <div
          class="ml-10 w-[480px] bg-gray-300 mr-5 rounded-3xl flex justify-center items-center p-5 h-[480px]"
        >
          <img
            :src="props.product.image"
            class="w-full h-full object-contain"
          />
        </div>
        <div class="w-1/2 pl-5">
          <p class="text-xl font-light mb-3">{{ props.product.category }}</p>
          <h1 class="text-4xl font-bold mb-3">{{ props.product.name }}</h1>
          <h3 class="text-4xl font-light mb-3">${{ props.product.price }}</h3>
          <p class="mb-10">{{ props.product.description }}</p>
          <div class="flex flex-col gap-4">
            <button class="btn btn-outline btn-primary">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
