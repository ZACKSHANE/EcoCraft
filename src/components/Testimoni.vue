<script setup>
const testimonials = [
  { name: 'Dian', stars: 4, text: '"Produk berkualitas, saya suka Totebagnya kuat dan unik"' },
  { name: 'Alex', stars: 5, text: '"Bangga bisa ikut berkontribusi buat lingkungan dengan beli produk ini.""' },
  { name: 'Rudi', stars: 5, text: '"Workshopnya seru, langsung praktek dan bisa bawa pulang hasil"' },
  { name: 'Hani', stars: 5, text: '"Saya beli tas daur ulang ini buat gantiin tas plastik. Selain modelnya keren, bahannya juga kuat dan awet. Recommended!"' }
]
</script>

<template>
  <section class="bg-[#317E30] pb-30">
    <h1 class="text-5xl text-center sm:text-left md:text-7xl text-white font-bold font-poppins px-15 py-10">
      Testimoni
    </h1>

    <div class=" grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-2 gap-8 px-4 justify-center justify-items-stretch">
      <div
        v-for="(item, index) in testimonials"
        :key="index"
        class="bg-white rounded-xl p-6 mx-0 sm:mx-10 inline-block w-full max-w-[620px]"
      >
        <h3 class="text-2xl font-semibold mb-2">{{ item.name }}</h3>

        <div class="flex mb-3 space-x-1">
          <svg
            v-for="i in item.stars"
            :key="i"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 39 39"
            fill="currentColor"
            class="w-8 h-8 text-yellow-400"
          >
            <path
              d="M19.5 28.0721L12.7562 32.1346C12.4583 32.3242 12.1469 32.4054 11.8219 32.3783C11.4969 32.3512 11.2125 32.2429 10.9687 32.0533C10.725 31.8637 10.5354 31.627 10.4 31.3432C10.2646 31.0594 10.2375 30.7409 10.3187 30.3877L12.1062 22.7096L6.13436 17.5502C5.86353 17.3064 5.69453 17.0286 5.62736 16.7166C5.56019 16.4046 5.58024 16.1002 5.68749 15.8033C5.79474 15.5065 5.95724 15.2627 6.17498 15.0721C6.39274 14.8814 6.69065 14.7595 7.06873 14.7064L14.95 14.0158L17.9969 6.78457C18.1323 6.45957 18.3424 6.21582 18.6274 6.05332C18.9123 5.89082 19.2032 5.80957 19.5 5.80957C19.7968 5.80957 20.0877 5.89082 20.3726 6.05332C20.6575 6.21582 20.8677 6.45957 21.0031 6.78457L24.05 14.0158L31.9312 14.7064C32.3104 14.7606 32.6083 14.8825 32.825 15.0721C33.0417 15.2617 33.2042 15.5054 33.3125 15.8033C33.4208 16.1012 33.4414 16.4062 33.3742 16.7182C33.3071 17.0302 33.1375 17.3075 32.8656 17.5502L26.8937 22.7096L28.6812 30.3877C28.7625 30.7398 28.7354 31.0583 28.6 31.3432C28.4646 31.6281 28.275 31.8648 28.0312 32.0533C27.7875 32.2418 27.5031 32.3502 27.1781 32.3783C26.8531 32.4065 26.5417 32.3252 26.2437 32.1346L19.5 28.0721Z"
            />
          </svg>
        </div>

        <p class="text-gray-700 text-base md:text-2xl">{{ item.text }}</p>
      </div>
    </div>
  </section>
</template>
