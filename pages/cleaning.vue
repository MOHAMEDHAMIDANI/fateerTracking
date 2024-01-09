<template>
    <MainLay>
        <div class="flex flex-col items-center w-full">
            <div class="flex items-center justify-around w-full h-16 my-5">
                <select class="outline-none w-[200px] h-9 rounded text-2xl capitalize bg-gray-100" name="meals"
                    v-model="type" id="">
                    <option value="Hawawshi Box">Hawawshi Box</option>
                    <option value="Box M">Box M</option>
                    <option value="Box L">Box L</option>
                    <option value="Box XL">Box XL</option>
                    <option value="cleaners">cleaners</option>
                    <option value="Foil / Stretch">Foil / Stretch</option>
                    <option value="tissue">tissue</option>
                    <option value="butter paper">butter paper</option>
                </select>
                <div class="flex flex-col items-center justify-center">
                    <input placeholder="Quantity" v-model="Qnt" type="text"
                        class="text-2xl text-black w-[200px] h-9 rounded outline-none pl-2 bg-gray-100">
                </div>
                <div class="flex flex-col items-center justify-center">
                    <input placeholder="price" v-model="Price" type="text"
                        class=" capitalize text-2xl text-black w-[200px] h-9 rounded outline-none pl-2 bg-gray-100">
                </div>
            </div>
            <button @click="addToTable()"
                class="w-[100px] text-xl capitalize text-white h-9 bg-red-200 bg-gradient-to-r from-50% hover:opacity-80 duration-500 from-red-400 to-yellow-400 rounded ">submit</button>
        </div>
        <div class="mt-5">
            <table>
                <tr class="bg-gradient-to-r from-50% from-red-400 to-yellow-400 text-white text-2xl mx-2 px-3">
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-x-2 text-center border-black">date</th>
                    <th class="min-w-[250px] h-10 capitalize border-x-2 text-center border-black w-[400px]">type</th>
                    <th class="min-w-[250px] h-12 capitalize border-x-2 text-center border-black w-[400px]">Qnt</th>
                    <th class="min-w-[250px] h-10 capitalize border-x-2 text-center border-black w-[400px]">Price</th>
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-x-2 text-center border-black">total</th>
                </tr>
                <div v-if="wait">wait</div>
                <tr v-else v-for="data in clean">
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-2 text-center border-black">{{ data.date }}</th>
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-2 text-center border-black">{{ data.type }}</th>
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-2 text-center border-black">{{ data.Qnt }}</th>
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-2 text-center border-black">{{ data.Price }}
                    </th>
                    <th class="min-w-[250px] w-[400px] h-10 capitalize border-2 text-center border-black">{{ data.total }}
                    </th>
                </tr>
            </table>
        </div>
    </MainLay>
</template>

<script setup lang="ts">
import MainLay from '../layouts/MainLay.vue'
const wait = ref(false)
const dateOptions = ref({ year: "numeric", month: "short", day: "numeric" });
const type = ref('Box M')
const Qnt = ref('')
const Price = ref('')
let clean = []; // Initialize sugar as a ref with an empty array

onBeforeMount(() => {
    const storedclean = localStorage.getItem('clean');
    clean = storedclean ? JSON.parse(storedclean) : []; // Assign the parsed value to sugar.value
});

const addToTable = () => {
    wait.value = true;
    const currentDate = new Date(Date.now()).toLocaleDateString("en-us", dateOptions);
    let temporary = {
        date: `${currentDate}`,
        type: `${type.value}`,
        Qnt: `${Qnt.value}`,
        Price: `${Price.value}`,
        total: `${Price.value * Qnt.value} QR`,
    };
    clean.push(temporary); // Access sugar as a ref using sugar.value
    localStorage.setItem('clean', JSON.stringify(clean));
    wait.value = false;
};
</script>

<style scoped></style>