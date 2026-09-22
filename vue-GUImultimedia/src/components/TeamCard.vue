<template>
  <div class="about-page">

    <!-- CERITA KAMI -->
    <section class="story">
      <div class="story-text">
        <h1>Cerita Kami</h1>

        <p>
          Toko kami bermula dari sebuah ide sederhana untuk menyediakan
          produk yang berkualitas dan mudah dijangkau oleh semua orang.
        </p>

        <p>
          Dengan semangat untuk terus berkembang, kami berusaha memberikan
          pengalaman belanja yang nyaman, cepat, dan terpercaya bagi setiap
          pelanggan.
        </p>
      </div>

      <div class="story-image">
        <div class="image-placeholder">
          🏪
        </div>
      </div>
    </section>


    <!-- TIM KAMI -->
    <section class="team">
      <h2>Tim Kami</h2>

      <p class="team-description">
        Kenali orang-orang yang bekerja bersama untuk memberikan pelayanan
        terbaik kepada pelanggan.
      </p>

      <div class="team-container">
        <TeamCard
          v-for="anggota in daftarTim"
          :key="anggota.id"
          :nama="anggota.nama"
          :jabatan="anggota.jabatan"
        />
      </div>
    </section>

  </div>
</template>

<script setup>
import TeamCard from "../components/TeamCard.vue"

const daftarTim = [
  {
    id: 1,
    nama: "Andi",
    jabatan: "Founder"
  },
  {
    id: 2,
    nama: "Budi",
    jabatan: "Marketing"
  },
  {
    id: 3,
    nama: "Citra",
    jabatan: "Customer Service"
  }
]
</script>

<style scoped>
.about-page {
  min-height: 100vh;
  background: #f4f7f6;
}

/* CERITA KAMI */
.story {
  display: flex;
  align-items: center;
  gap: 50px;
  padding: 70px 10%;
  background: white;
}

.story-text {
  flex: 1;
}

.story-text h1 {
  margin-bottom: 20px;
  color: #1f2937;
  font-size: 40px;
}

.story-text p {
  margin-bottom: 15px;
  color: #6b7280;
  line-height: 1.7;
}

.story-image {
  flex: 1;
}

.image-placeholder {
  height: 280px;

  display: flex;
  align-items: center;
  justify-content: center;

  border-radius: 20px;
  background: linear-gradient(135deg, #0f766e, #2563eb);

  color: white;
  font-size: 80px;
}


/* TIM KAMI */
.team {
  padding: 60px 20px;
  text-align: center;
}

.team h2 {
  margin-bottom: 10px;
  color: #1f2937;
  font-size: 32px;
}

.team-description {
  margin-bottom: 35px;
  color: #6b7280;
}

.team-container {
  display: flex;
  justify-content: center;
  gap: 25px;
  flex-wrap: wrap;
}
</style>
defineProps()