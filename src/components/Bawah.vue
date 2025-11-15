<script setup>
import logo from "@/assets/logos.png";
</script>

<template>
  <section
    class="w-full bg-cover bg-center px-5 md:px-20 py-16"
    style="background-image: url('/bgfooter.jpg'); background-position: bottom;"
  >
   
    <div class="bg-[#C0965B]/80 p-5 md:p-10">

      <div class="grid md:grid-cols-2 gap-10 items-center text-center md:text-left">

      
        <div class="flex flex-col items-center md:items-start">
          <img :src="logo" alt="" class="w-[85px] h-[85px] mb-4">
          <p class="text-xl md:text-2xl text-amber-50 font-extrabold font-poppins leading-snug">
            Eco Craft: Sentuhan Tangan,<br />
            Nilai Tak Tergantikan.
          </p>
        </div>

        <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 md:gap-6 text-white font-poppins font-semibold text-lg md:text-3xl">
          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Home</a>
          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Workshop</a>
          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Produk</a>

          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Tentang</a>
          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Galeri</a>
          <a href="#" class="hover:bg-amber-500 hover:rounded-md hover:px-2 md:hover:px-5 py-1">Kontak</a>
        </div>

      </div>

  
      <div class="border-t border-black mt-8"></div>

     
      <p class="text-center text-white font-poppins text-base md:text-2xl font-black mt-4">
        © 2018 Eco Craft — Semua hak dilindungi
      </p>

    </div>
  </section>
</template>
