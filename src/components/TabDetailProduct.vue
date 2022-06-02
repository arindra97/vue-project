<template>
    <div>
        <div class="container mx-auto">
            <!-- Tab -->
            <ul class="flex justify-start text-sky-500">
                <li>
                    <button @click="currentTab(1)"
                        class="inline-block px-4 py-2 border-b-2 border-sky-500 focus:outline-none focus:font-bold focus:bg-sky-100">
                        Ringkasan Harga
                    </button>
                </li>
                <li>
                    <button @click="currentTab(2)"
                        class="inline-block px-4 py-2 border-b-2 border-sky-500 focus:outline-none focus:font-bold focus:bg-sky-100">
                        Deskripsi
                    </button>
                </li>
            </ul>
            <div class="px-2 mt-2 flex flex-col">
                <!-- Tab Ringkasan Harga -->
                <div v-if="tab === 1">
                    <div class="my-4 grid grid-cols-4">
                        <p class="col-span-1 font-semibold">Varian</p>
                        <p class="col-span-3">Black</p>
                    </div>

                    <div class="my-4 grid grid-cols-4">
                        <p class="col-span-1 font-semibold">Pilih Tipe</p>
                    </div>
                    
                    <table class="container w-full table-auto md:table-fixed">
                        <thead>
                            <tr>
                                <th class="w-1/2 px-4 py-2">Tipe</th>  
                                <th class="w-1/8 px-4 py-2">Harga</th>  
                                <th class="w-1/8 px-4 py-2">Stok</th>  
                                <th class="w-1/4 px-4 py-2">Jumlah Order</th>  
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td class="px-4 py-2">Black - New 13.3Air A1932/A2179/A2337</td>
                                <td class="px-4 py-2 text-center">Rp 36,916</td>
                                <td class="px-4 py-2 text-center">9,000 Stok</td>
                                <td class="px-4 py-2">
                                    <div class="flex flex-row items-center justify-center space-x-2">
                                        <button class="w-10 border  bg-gray-200 rounded py-2" @click="decrement">-</button>
                                        <div class="shadow appearance-none w-1/3 text-center border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">{{ count }}</div>
                                        <button class="w-10 border bg-gray-200 rounded py-2" @click="increment">+</button>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="px-4 py-2">Black - New 13.3 Pro (13.3Pro A1706/A1708/A1989/A2159/A2338)</td>
                                <td class="px-4 py-2 text-center">Rp 36,916</td>
                                <td class="px-4 py-2 text-center">10,000 Stok</td>
                                <td class="px-4 py-2">
                                    <div class="flex flex-row items-center justify-center space-x-2">
                                        <button class="w-10 border  bg-gray-200 rounded py-2" @click="decrement">-</button>
                                        <div class="shadow appearance-none w-1/3 text-center border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">{{ count }}</div>
                                        <button class="w-10 border bg-gray-200 rounded py-2" @click="increment">+</button>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="px-4 py-2">Black - New Pro14 A2442</td>
                                <td class="px-4 py-2 text-center">Rp 36,916</td>
                                <td class="px-4 py-2 text-center">10,000 Stok</td>
                                <td class="px-4 py-2">
                                    <div class="flex flex-row items-center justify-center space-x-2">
                                        <button class="w-10 border  bg-gray-200 rounded py-2" @click="decrement">-</button>
                                        <div class="shadow appearance-none w-1/3 text-center border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">{{ count }}</div>
                                        <button class="w-10 border bg-gray-200 rounded py-2" @click="increment">+</button>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="px-4 py-2">Black - 2020 13.3Pro (A2251/A2289)</td>
                                <td class="px-4 py-2 text-center">Rp 36,916</td>
                                <td class="px-4 py-2 text-center">10,000 Stok</td>
                                <td class="px-4 py-2">
                                    <div class="flex flex-row items-center justify-center space-x-2">
                                        <button class="w-10 border  bg-gray-200 rounded py-2" @click="decrement">-</button>
                                        <div class="shadow appearance-none w-1/3 text-center border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">{{ count }}</div>
                                        <button class="w-10 border bg-gray-200 rounded py-2" @click="increment">+</button>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="px-4 py-2">Black - New Pro16 A2485</td>
                                <td class="px-4 py-2 text-center">Rp 41,259</td>
                                <td class="px-4 py-2 text-center">10,000 Stok</td>
                                <td class="px-4 py-2">
                                    <div class="flex flex-row items-center justify-center space-x-2">
                                        <button class="w-10 border  bg-gray-200 rounded py-2" @click="decrement">-</button>
                                        <div class="shadow appearance-none w-1/3 text-center border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">{{ count }}</div>
                                        <button class="w-10 border bg-gray-200 rounded py-2" @click="increment">+</button>
                                    </div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                    
                    <div class="mt-8 my-4 grid grid-cols-4">
                        <p class="col-span-1 font-semibold">Ringkasan Harga</p>
                        <div class="col-span-3">
                            <div class="my-2 grid grid-cols-3">
                                <p class="col-span-2">Harga Produk X {{ count }}</p>
                                <p class="col-span-1">Rp 0</p>
                            </div>

                            <div class="my-2 grid grid-cols-3">
                                <p class="col-span-2">Handling Fee 3%</p>
                                <p class="col-span-1">Rp 0</p>
                            </div>

                            <div class="my-2 grid grid-cols-3">
                                <p class="col-span-2">Ongkir Lokal China</p>
                                <div class="flex flex-row space-x-2">
                                    <p class="col-span-1">Rp -</p>
                                    <button type="button" class="border border-solid border-sky-500 hover:bg-sky-400 active:bg-sky-600 px-2 py-1 rounded outline-none focus:outline-none ease-linear transition-all duration-150">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="fill-sky-500 hover:fill-white bi bi-info-circle" viewBox="0 0 16 16"> <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/> <path d="m8.93 6.588-2.29.287-.082.38.45.083c.294.07.352.176.288.469l-.738 3.468c-.194.897.105 1.319.808 1.319.545 0 1.178-.252 1.465-.598l.088-.416c-.2.176-.492.246-.686.246-.275 0-.375-.193-.304-.533L8.93 6.588zM9 4.5a1 1 0 1 1-2 0 1 1 0 0 1 2 0z"/> </svg>
                                    </button>
                                </div> 
                            </div>
                            
                            <div class="my-2 grid grid-cols-3">
                                <p class="col-span-2">Ongkir China ke Indonesia</p>
                                <div class="flex flex-row space-x-2">
                                    <p class="col-span-1">Rp -</p>
                                    <button type="button" class="border border-solid border-sky-500 hover:bg-sky-400 active:bg-sky-600 px-2 py-1 rounded outline-none focus:outline-none ease-linear transition-all duration-150">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="fill-sky-500 hover:fill-white bi bi-info-circle" viewBox="0 0 16 16"> <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/> <path d="m8.93 6.588-2.29.287-.082.38.45.083c.294.07.352.176.288.469l-.738 3.468c-.194.897.105 1.319.808 1.319.545 0 1.178-.252 1.465-.598l.088-.416c-.2.176-.492.246-.686.246-.275 0-.375-.193-.304-.533L8.93 6.588zM9 4.5a1 1 0 1 1-2 0 1 1 0 0 1 2 0z"/> </svg>
                                    </button>
                                </div> 
                            </div>
                        </div>
                    </div>
                </div>
                
                
                <!-- Tab Desckripsi -->
                <div v-if="tab === 2">
                    <h2 class="flex justify-center text-sm md:text-lg mb-2">Detail Produk</h2>
                    <div class="max-w-full">
                        <img class="w-full" src="../assets/deskripsi/desc1.jpg" alt="">
                        <img class="w-full" src="../assets/deskripsi/desc2.jpg" alt="">
                        <img class="w-full" src="../assets/deskripsi/desc3.jpg" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    setup() {
        const tab = ref(1);
        const currentTab = (tabNumber) => (tab.value = tabNumber);
        return { tab, currentTab };
    },
    data() {
        return {
        count: 0
        }
    },
    methods: {
        increment() {
            this.count++
        },
        decrement() {
            this.count--
        }
    }
};
</script>