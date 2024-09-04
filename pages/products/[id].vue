<template>
    <div>
        <p>Product ID: {{id}}</p>

        <div class="bg-white shadow-sm p-4">
            <h2>{{ product.title }}</h2>
            <p>${{ product.price }}</p>
            <p>{{ product.description }}</p>
            <img :src="product.image" alt="product.title" class="size-1/4 mx-auto"/>
        </div>

    </div>
</template>

<script setup>
    const { id } = useRoute().params;

    const { data: product } = await useFetch(`https://fakestoreapi.com/products/${id}`);

    definePageMeta({
        layout: 'default'
    });

</script>

