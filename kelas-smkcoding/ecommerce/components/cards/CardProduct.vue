<script lang="ts" setup>
const props = defineProps({
  product: {
    type: Object,
    default: {},
  },
});
</script>

<template>
  <div class="card w-120 h-auto bg-base-100 shadow-xl">
    <figure>
      <img
        :src="props.product.image"
        alt="Shoes"
        class="w-36 h-36 object-cover"
      />
    </figure>
    <div class="card-body">
      <NuxtLink :to="`/product/${props.product.id}`">
        <h1 class="card-title text-xl">{{ props.product.name }}</h1>
        <p class="text-md">{{ props.product.category }}</p>
        <p class="text-lg">{{ props.product.price }}$</p>
      </NuxtLink>
      <div class="card-actions justify-end">
        <button class="btn btn-primary text-xs">Add to cart</button>
      </div>
    </div>
  </div>
</template>
