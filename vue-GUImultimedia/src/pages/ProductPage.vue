<script setup>
import ProductCard from '../components/ProductCard.vue'
 
const daftarProduk = [
  { id: 1, nama: 'brithis', harga: 15.500000, gambar: 
'https://www.bing.com/images/search?view=detailV2&ccid=qP8E0wqf&id=68605A7C3F4411BC26AE7F12CF97DAAD51DD1F19&thid=OIP.qP8E0wqf5a-SXz1RNFon_gHaE7&mediaurl=https%3a%2f%2fi.pinimg.com%2foriginals%2fa9%2f2d%2f33%2fa92d331ae8bced8ad8d4b91210d80110.jpg&exph=2634&expw=3958&q=motor+british+style&mode=overlay&FORM=IQFRBA&ck=B99C3F9663A68D4EC71EECE517E3B1C9&selectedIndex=0&idpp=serp' },
  { id: 2, nama: 'Topi Sekolah', harga: 35000, gambar: 
'https://placehold.co/150' },
  { id: 3, nama: 'Tas Sekolah', harga: 120000, gambar: 
'https://placehold.co/150' },
]
</script>
 
<template>
  <main>
    <h1>Produk Kami</h1>
    <div class="grid">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />
    </div>
  </main>
  </template>
  <style scoped>
.grid {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}
</style>