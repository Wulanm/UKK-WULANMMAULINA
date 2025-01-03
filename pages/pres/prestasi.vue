<template>
    <div>
      <section class="prestasi-container py-10 bg-gray-100">
        <div class="container mx-auto px-4">
          <h1 class="text-center text-3xl font-bold mb-8">Prestasi Kami</h1>
  
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Loop untuk menampilkan prestasi -->
            <div v-for="(prestasi, index) in prestasiList" :key="index" class="prestasi-item bg-white rounded-lg shadow-md overflow-hidden">
              <img :src="prestasi.image" alt="Prestasi" class="w-full h-56 object-cover">
              <div class="p-4">
                <h3 class="text-xl font-semibold mb-2">{{ prestasi.title }}</h3>
                <p class="text-gray-700">{{ prestasi.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PrestasiPage',
    data() {
      return {
        prestasiList: [
          {
            title: 'Juara 1 Lomba Sains',
            description: 'SMKN 4 Tasikmalaya meraih Juara 1 dalam Lomba Sains tingkat Provinsi Jawa Barat.',
            image: require('~/assets/img/Expo-Creanova-1.webp') // Gambar lokal
          },
          {
            title: 'Juara 2 Lomba Desain Grafis',
            description: 'Siswa kami berhasil meraih Juara 2 dalam lomba desain grafis tingkat Nasional.',
            image: require('~/assets/img/ujiansekolah.jpg') // Gambar lokal
          },
          {
            title: 'Juara 3 Lomba Robotik',
            description: 'Tim Robotik kami meraih Juara 3 dalam kompetisi robotik internasional.',
            image: require('@/assets/img/honda.jpeg') // Gambar lokal
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* Styling untuk halaman prestasi */
  .prestasi-container {
    background-color: #f9fafb;
  }
  
  .prestasi-item {
    transition: transform 0.3s ease;
  }
  
  .prestasi-item:hover {
    transform: translateY(-10px);
  }
  
  .prestasi-item img {
    object-fit: cover;
  }
  
  h1 {
    color: #333;
  }
  
  h3 {
    color: #2d3748;
  }
  </style>
  
  
  