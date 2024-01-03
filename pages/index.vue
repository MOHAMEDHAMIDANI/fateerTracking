<template>
    <MainLay>
        <div class="w-full min-h-[700px] flex justify-center items-center">
            <nuxt-link :to="{name : 'meat'}">
                <div class="w-[200px] h-[200px] bg-red-400 relative rounded overflow-hidden">
                    <h3 class="absolute top-0 left-0  z-10 w-full  flex justify-center items-center  text-center text-5xl text-white h-full">لحوم </h3>
                    <img src="../assets/download.jpg" alt="" class="w-full  h-full absolute top-0 left-0">
                </div>
            </nuxt-link>
        </div>
    </MainLay>
</template>

<script setup lang="ts">
import MainLay from '../layouts/MainLay.vue'
</script>

<style scoped>

</style>