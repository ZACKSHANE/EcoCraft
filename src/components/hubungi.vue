<script setup>
import Instagram from "@/assets/ig.png";
import fabe from "@/assets/fabe.png";
import tiktok from "@/assets/tiktok1.png";
import mail from "@/assets/mail.png";
import tp from "@/assets/telpon .png";
</script>

<template>
  <section class="bg-[#F7F9DC] py-20 px-10 md:px-20" id="kontak">
    
    <h2 class="text-4xl md:text-5xl font-extrabold font-poppins mb-4">
      Hubungi Kami
    </h2>

 
    <p class="text-xl font-medium mb-10">
      Alamat: <span class="font-normal">Jl. Hijau Lestari No. 23, Yogyakarta</span>
    </p>

   
    <div class="grid md:grid-cols-2 gap-10 items-start justify-center text-center md:text-left">
     
      <div>
        <h3 class="text-2xl font-semibold mb-4">Media Sosial:</h3>
        <ul>
          <li class="flex items-center   "><img :src="Instagram" alt="" class=" w-[58px] h-[54px] bg-[#ffff] rounded-full py-1 px-1 mb-2">
          <p class=" pl-2 pb-2 text-2xl font-semibold font-poppins">Instagram: EcoCraft.id</p></li>
          <li class=" flex items-center"><img :src="fabe" alt="" class=" w-[58px] h-[54px]  bg-[#ffff] rounded-full py-1 px-1 mb-2" >
         <p class=" pl-2 pb-2 text-2xl font-semibold font-poppins"> Facebook: EcoCraft.id</p></li>
          <li class="flex items-center"><img :src="tiktok" alt="" class=" w-[58px] h-[54px] bg-[#ffff] rounded-full py-1 px-1">
          <p class=" pl-2 pb-2 text-2xl font-semibold font-poppins">TikTok: EcoCraft.id</p></li>
        </ul>
      </div> 

     
      <div>
        <h3 class="text-2xl font-semibold mb-4">Media Sosial:</h3>
        <ul>
          <li class="flex items-center   "><img :src="mail" alt="" class=" w-[58px] h-[54px] bg-[#ffff] rounded-full py-1 px-1 mb-2">
          <p class=" pl-2 pb-2 text-2xl font-semibold font-poppins">halo@ecocraft.id</p></li>
          <li class=" flex items-center"><img :src="tp" alt="" class=" w-[58px] h-[54px]  bg-[#ffff] rounded-full py-1 px-1 mb-2" >
         <p class=" pl-2 pb-2 text-2xl font-semibold font-poppins"> 0812 3456 7890</p></li>
        </ul>
      </div> 
    </div>
  </section>
</template>
