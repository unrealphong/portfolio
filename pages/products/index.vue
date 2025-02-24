<template>
	<div class="flex flex-col items-center">
		<h1 class="text-4xl text-red-500">
			Danh sách sản phẩm
		</h1>
		<ul>
			<li
				v-for="product in products"
				:key="product.id"
			>
				<NuxtLink :to="`/products/${product.id}`">{{ product.name }}</NuxtLink>
			</li>
		</ul>
	</div>
</template>

<script setup>
const products = [
	{ id: 1, name: 'Sản phẩm A' },
	{ id: 2, name: 'Sản phẩm B' },
	{ id: 3, name: 'Sản phẩm C' },
];
</script>
