<script setup>
import { ref, onMounted } from "vue";

const videos = [
  "https://www.youtube.com/embed/MtLC4FnnkWg",
  "https://www.youtube.com/embed/bDus7YXtOIg",
  "https://www.youtube.com/embed/HeT9cNY-i6Q",
  "https://www.youtube.com/embed/NSsDOcT5p-4",
  "https://www.youtube.com/embed/rgh_hI712bI",
];

const index = ref(0);

onMounted(() => {
  setInterval(() => {
    index.value = (index.value + 1) % videos.length;
  }, 3000); 
});


function getStyle(i) {
  const total = videos.length;
  const diff = (i - index.value + total) % total;

  if (diff === 0) {
  
    return {
      transform: "translateX(0) scale(1.15) rotateY(0deg)",
      zIndex: 3,
      opacity: 1,
    };
  } else if (diff === 1) {
    
    return {
      transform: "translateX(260px) scale(0.85) rotateY(-35deg)",
      zIndex: 2,
      opacity: 0.8,
    };
  } else if (diff === total - 1) {
    
    return {
      transform: "translateX(-260px) scale(0.85) rotateY(35deg)",
      zIndex: 2,
      opacity: 0.8,
    };
  } else {
   
    return {
      transform: "translateX(0) scale(0.6) rotateY(0deg)",
      zIndex: 1,
      opacity: 0.3,
    };
  }
}
</script>

<template>
  <section id="workshop"
    class="w-full min-h-screen bg-cover bg-center relative px-6 md:px-20 py-16"
    style="background-image: url('/workshop.jpg'); background-position: bottom;"
  >
    
    <h1 class="text-left font-bold text-4xl font-poppins mb-16 text-black">
      Workshop & Tutorial
    </h1>

    <div class="relative w-full flex justify-center overflow-hidden py-10">
      <div class="relative w-full h-[420px] flex items-center justify-center perspective-1000">
      
        <div
          v-for="(video, i) in videos"
          :key="i"
          class="absolute transition-all duration-[900ms] ease-in-out"
          :style="getStyle(i)"
        >
          <iframe
            :src="video"
            class="rounded-xl shadow-2xl w-[330px] h-[250px] md:w-[400px] md:h-[300px]"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>

    <div>
      <ul class="text-3xl text-black pt-20">
        Kami menyelenggarakan workshop tatap muka dan online:
        <li class="list-disc ml-15">
          Workshop pemula: Membuat tas dari kain perca (durasi 2 jam)
        </li>
        <li class="list-disc ml-15">
          Workshop lanjutan: Lampu hias dari botol (durasi 3 jam)
        </li>
        <li class="list-disc ml-15 pb-20">
          Tutorial video: 10 cara mengubah kardus jadi dekorasi
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.perspective-1000 {
  perspective: 1000px;
}
</style>
