<script setup>
import { ref } from "vue";

const isOpen = ref(false);
</script>

<template>
  <header class="w-full bg-[#317E30] py-3 px-8 flex items-center justify-between">
    <div>
      <img
        src="/src/assets/logos.png"
        alt="EcoCraft"
        class="w-[85px] h-[85px] object-contain"
      />
    </div>
    <button @click="isOpen = !isOpen" class="md:hidden text-white text-3xl focus:outline-none">
      ☰
    </button>

    <nav class="hidden md:flex gap-6 text-white font-medium">
      <a href="#home" class="font-poppins text-[20px] text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[100px] hover:px-5">Home</a>
      <a href="#tentang" class="font-poppins text-xl text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[120px] hover:px-5">Tentang</a>
      <a href="#workshop" class="font-poppins text-xl text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[150px] hover:px-5">Workshop</a>
      <a href="#gallery" class="font-poppins text-xl text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[100px] hover:px-5">Galeri</a>
      <a href="#kontak" class="font-poppins text-xl text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[100px] hover:px-5">Kontak</a>
      <a href="#produk" class="font-poppins text-xl text-[#FFFFFF] font-normal hover:bg-amber-500 hover:rounded-md hover:w-[110px] hover:px-5">Produk</a>
    </nav>
  </header>

  <transition name="slide-right">
    <div
      v-if="isOpen"
      class="fixed top-0 right-0 h-full w-[200px] bg-[#317E30]/80 text-white flex flex-col gap-6 p-8 z-50 shadow-xl"
    >
      <button class="text-3xl self-end mb-4" @click="isOpen = false">✕</button>

      <a href="#home" @click="isOpen=false" class="text-xl">Home</a>
      <a href="#tentang" @click="isOpen=false" class="text-xl">Tentang</a>
      <a href="#workshop" @click="isOpen=false" class="text-xl">Workshop</a>
      <a href="#gallery" @click="isOpen=false" class="text-xl">Galeri</a>
      <a href="#kontak" @click="isOpen=false" class="text-xl">Kontak</a>
      <a href="#produk" @click="isOpen=false" class="text-xl">Produk</a>
    </div>
  </transition>
</template>

<style scoped>
html {
  scroll-behavior: smooth;
}

.slide-right-enter-active,
.slide-right-leave-active {
  transition: transform 0.3s ease;
}

.slide-right-enter-from,
.slide-right-leave-to {
  transform: translateX(100%);
}
</style>
