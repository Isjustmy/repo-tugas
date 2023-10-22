<template>
  <div class="hero bg-base-200 min-h-screen flex flex-col">
    <div class="hero-content flex-col lg:flex-row-reverse mt-10">
      <img
        src="../public/shop.png"
        class="max-w-sm rounded-lg"
      />
      <div class="w-[600px] mr-[60px]">
        <h1 class="text-5xl font-bold">Selamat Datang di SMKCoding Store!</h1>
        <p class="py-6 w-[500px]">
          Di website ini kalian bisa belanja berbagai macam kebutuhan fashion mulai dari Baju, Celana, Sepatu, Jam Tangan, dan lain lain.
        </p>
        <NuxtLink :to="'/product'">
          <button class="btn btn-primary">Cek Produk!</button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
