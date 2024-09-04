<template>
    <p>Products</p>

    <div>
        <div class="grid grid-cols-3 gap-4">
            <div v-for="p in products" class="p-4">
                <ProductCard :product="p" />
            </div>
        </div>
    </div>

</template>

<script setup>
    definePageMeta({
        layout: 'default'
    });

    const { data: products } = await useFetch('https://fakestoreapi.com/products');

</script>