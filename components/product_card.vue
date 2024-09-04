<template>
    <div class = "card text-center shadow bg-white p-4">
        <NuxtLink :to="`/products/${product.id}`">
            <p class="truncate m-4 font-bold text-gray-500">{{ product.title }}</p>
            <img :src="product.image" alt="product.title" class="size-1/2 mx-auto m-8"/>
            <p class="bg-lime-400 w-3/4 mx-auto h-10 flex items-center justify-center text-lg rounded-lg">${{ product.price }}</p>
        </NuxtLink>
    </div>
</template>

<script setup>

    const { product } = defineProps(['product']);

</script>

<style scoped>

</style>