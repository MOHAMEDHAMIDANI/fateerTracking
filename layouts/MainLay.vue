<template>
    <div class="min-h-screen min-w-screen">
        <nuxt-link to="/">
        <nav class="flex items-center justify-center w-full shadow-md h-14">
                <h3 class="w-full bg-gradient-to-r from-50% from-red-400 to-yellow-400 text-4xl text-center bg-clip-text text-transparent h-full mt-2 font-semibold cursor-pointer">Fateer Tracking </h3>
            </nav>
        </nuxt-link>
        <div class="w-full h-full bg-white/3">
            <slot />
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>