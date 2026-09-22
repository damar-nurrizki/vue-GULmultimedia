 <template>
  <div class="home">

    <!-- HERO -->
    <section class="hero">
      <div class="hero-content">
        <h1>Temukan Produk Terbaik Untukmu</h1>

        <p>
          Jelajahi berbagai produk pilihan dengan kualitas terbaik
          dan pengalaman belanja yang mudah.
        </p>

        <RouterLink to="/product" class="btn-product">
          Lihat Produk
        </RouterLink>
      </div>
    </section>

  
    <!-- FITUR -->
    <section class="features">
      <h2>Kenapa Memilih Kami?</h2>

      <div class="feature-container">

        <!-- v-for -->
        <div
          v-for="fitur in fiturList"
          :key="fitur.id"
          class="feature-card"
        >
          <div class="icon">
            {{ fitur.icon }}
          </div>

          <h3>{{ fitur.judul }}</h3>

          <p>{{ fitur.deskripsi }}</p>
        </div>

      </div>
    </section>

  </div>

</template>
<style scoped>
.home {
  min-height: 100vh;
  background: #f4f7f6;
}

/* HERO */
.hero {
  padding: 80px 20px;
  text-align: center;
  color: white;
  background: linear-gradient(135deg, #f6f7f7, #2563eb, #f6f7f7);
  
}

.hero h1 {
  font-size: 40px;
  margin-bottom: 15px;
}

.hero p {
  margin-bottom: 25px;
}

/* BUTTON */
.btn-product {
  display: inline-block;
  padding: 12px 28px;
  background: white;
  color: #2563eb;
  border-radius: 999px;
  text-decoration: none;
  font-weight: bold;
  transition: 0.3s;
}

.btn-product:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}

/* FITUR */
.features {
  padding: 50px 20px;
  text-align: center;
  background: linear-gradient(135deg, #f6f7f7, #2563eb, #f6f7f7);
  margin-top: 20px;
}

.features h2 {
  margin-bottom: 30px;
  color: #1f2937;
}

/* CONTAINER 3 CARD */
.feature-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

/* CARD */
.feature-card {
  width: 250px;
  padding: 25px;
  text-align: center;
  background: rgb(255, 255, 255);
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
  transition: 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.icon {
  font-size: 35px;
  margin-bottom: 10px;
}

.feature-card h3 {
  color: #1f2937;
  margin-bottom: 10px;
}

.feature-card p {
  color: #6b7280;
  line-height: 1.5;
}

</style>

<script>
export default {
  data() {
    return {
      fiturList: [
        {
          id: 1,
          icon: "🚀",
          judul: "Cepat",
          deskripsi: "Nikmati proses yang cepat dan mudah saat menggunakan layanan kami."
        },
        {
          id: 2,
          icon: "⭐",
          judul: "Berkualitas",
          deskripsi: "Kami menyediakan produk pilihan dengan kualitas terbaik."
        },
        {
          id: 3,
          icon: "🔒",
          judul: "Terpercaya",
          deskripsi: "Data dan transaksi kamu akan selalu kami jaga dengan aman."
        }
      ]
    }
  }
}
</script>
