<template>
    <MainLay>
        <div class="w-full flex flex-col items-center">
            <div class="h-16 w-full  my-5 flex justify-around items-center">
                <select class="outline-none w-[200px] h-9 rounded text-2xl capitalize bg-gray-100" name="meals" id="">
                    <option value="">meat</option>
                    <option value="">meat</option>
                    <option value="">meat</option>
                </select>
                <div class="flex flex-col justify-center items-center">
                    <input placeholder="Quantity" type="text" class="text-2xl text-black w-[200px] h-9 rounded outline-none pl-2 bg-gray-100">
                </div>
                <div class="flex flex-col justify-center items-center">
                    <input placeholder="price" type="text" class=" capitalize text-2xl text-black w-[200px] h-9 rounded outline-none pl-2 bg-gray-100">
                </div>
            </div>
            <button class="w-[100px] text-xl capitalize text-white h-9 bg-red-200 bg-gradient-to-r from-50% hover:opacity-80 duration-500 from-red-400 to-yellow-400 rounded ">submit</button>
        </div>
        <div class="mt-5">
            <table>
                <tr class="bg-gradient-to-r from-50% from-red-400 to-yellow-400 text-white text-2xl">
                  <th class="min-w-[250px] h-10 capitalize border-x-2 text-center border-black w-[400px]">type</th>
                  <th class="min-w-[250px] h-12 capitalize border-x-2 text-center border-black w-[400px]">Qnt</th>
                  <th class="min-w-[250px] h-10 capitalize border-x-2 text-center border-black w-[400px]">Price</th>
                  <th class="min-w-[250px] w-[400px] h-10 capitalize border-x-2 text-center border-black">total</th>
                </tr>
              </table>
        </div>
    </MainLay>
</template>

<script setup lang="ts">
import MainLay from '../layouts/MainLay.vue'

</script>

<style scoped>

</style>