<script setup>
defineProps([`nama`,`harga`,`gambar`])
</script>

<template>
    <div class="card">
        <img :src="gambar" :alt="nama"/>
        <h3>{{ nama }}</h3>
        <p>{{ harga.toLocaleString(`id-ID`) }}</p>
    </div>
</template>
<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 14px;
  width: 200px;
  text-align: center;
  box-shadow: 10px 10px 20px rgb(68, 68, 68);
  background-color: rgb(148, 236, 160);
}
.card img {
  width: 100%;
  border-radius: 6px;
  
}
</style>