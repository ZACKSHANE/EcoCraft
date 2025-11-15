<script setup>
import galey from "@/assets/galery.jpeg";
</script>

<template>
  <section class="flex flex-col md:flex-row items-start justify-between " id="gallery">

    <div class=" flex justify-center">
      <img
        :src="galey"
        alt="Galeri Kreasi"
        class=" w-[1000px] h-[545px] object-cover"
      />
    </div>

    <div class=" bg-[#315F30] text-white p-9 shadow-lg mx-auto items-center text-center flex flex-col">
      <h2 class="text-2xl font-bold mb-4 bg-[#F7F9DC] text-[#1C351D] w-fit px-10 py-1 rounded mx-auto">
        Galeri Kreasi
      </h2>
      <h3 class="text-xl font-semibold mb-3 mx-auto">Langkah-langkah:</h3>
      <ol class="text-[22px] list-decimal list-inside space-y-1 leading-relaxed">
        <li>Bersihkan stiker pada botol.</li>
        <li>Potong botol di bagian atas dan bawah.</li>
        <li>Masukkan kabel dari bagian atas botol.</li>
        <li>Lalu pasang fiting lampu di bagian atas <br> botol dan kencangkan dengan baut.</li>
        <li>Dan masukan lampu ke dalam botol dan <br>di pasangkan di fiting lampu nya.</li>
        <li>Jika lampu sudah terpasang, lalu <br> tempelkan ke tembok dengan baut.</li>
        <li>Dan terakhir nyalakan lampunya.</li>
      </ol>
    </div>
  </section>
</template>


<style scoped>
</style>
