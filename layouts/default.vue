<template>
    <div>
        <header class="shadow-sm bg-white">
        <h1>My Blog</h1>
        <nav class="container mx-auto p-4 flex justify-between">
            <NuxtLink to="/" class="font-bold">Crash Course</NuxtLink>
            <ul class="flex gap-4">
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink to="/products">Products</NuxtLink></li>
            </ul>
        </nav>
        </header>

        <div class="container mx-auto p-4">
            <slot />
        </div>

    </div>
</template>

<style scoped>

    .router-link-active {
        color: green;
    }

</style>