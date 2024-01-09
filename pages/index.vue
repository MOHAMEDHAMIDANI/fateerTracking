<template>
    <MainLay>
        <div class="min-w-full my-24 h-full gap-3 flex flex-cl justify-center items-center flex-wrap">
            <nuxt-link :to="{name : 'meat'}">
                <div class="shadow-lg min-w-[350px] h-[150px] bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">meat </h3> -->
                    <img src="../assets/photo-1607623814075-e51df1bdc82f.avif" alt="" class="absolute top-0 left-0 w-full h-full">
                </div>
            </nuxt-link>
            <nuxt-link :to="{name : 'milk'}">
                <div class="shadow-lg min-w-[350px] h-[150px] bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">milk </h3> -->
                    <img src="../assets/14-Dairy_Eggs_Cheese_1200X600_2.jpg" alt="" class="absolute top-0 left-0 w-full h-full">
                </div>
            </nuxt-link>
            <nuxt-link :to="{name : 'oil'}">
                <div class="min-w-[350px] h-[150px] shadow-lg bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">oil </h3> -->
                    <img src="../assets/2018_11_6_21_33_39_808.jpg" alt="" class="absolute top-0 left-0 w-full h-full">
                </div>
            </nuxt-link>
            <nuxt-link :to="{name : 'pasta'}">
                <div class="min-w-[350px] shadow-lg h-[150px] bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">pasta </h3> -->
                    <img src="../assets/الفرق-بين-الدقيق-الأبيض-ودقيق-القمح-الكامل.jpg" alt="" class="absolute top-0 left-0 w-full h-full">
                </div>
            </nuxt-link>
            <nuxt-link :to="{name : 'suger'}">
                <div class="min-w-[350px] shadow-lg h-[150px] bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">sugar </h3> -->
                    <img src="../assets/45022315_6.jpg" alt="" class="absolute top-0 left-0 w-full h-full">
                </div>
            </nuxt-link>
            <nuxt-link :to="{name : 'cleaning'}">
                <div class="min-w-[350px] shadow-lg h-[150px] bg-red-400 relative rounded overflow-hidden">
                    <!-- <h3 class="absolute top-0 left-0 z-10 flex items-center justify-center w-full h-full text-5xl text-center text-white">cleaning </h3> -->
                    <img src="../assets/636563622729286112.jpg" alt="" class="absolute top-0 left-0 w-full h-full">
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