<template>
  <div>
    <h1>Chi tiết sản phẩm</h1>
    <p>ID: {{ id }}</p>
    <p>Tên sản phẩm: {{ product?.name }}</p>
    <NuxtLink to="/products">⬅ Quay lại danh sách</NuxtLink>
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
const id = route.params.id;

// Giả lập dữ liệu sản phẩm
const products = [
  { id: "1", name: "Sản phẩm A" },
  { id: "2", name: "Sản phẩm B" },
  { id: "3", name: "Sản phẩm C" },
];

// Tìm sản phẩm theo ID
const product = products.find((p) => p.id === id);
</script>
