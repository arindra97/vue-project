<script setup>
    import Navigasi from './components/navbar.vue'
    import Footer from './components/Footer.vue'
    import BreadCumb from './components/BreadCumb.vue'
    import CartIcon from './components/icons/IconCart.vue'
    import LoveIcon from './components/icons/IconLove.vue'
    import TabDetail from './components/TabDetailProduct.vue'
</script>

<template>
    <Navigasi />
    <BreadCumb class="mt-8 mb-4"/>

    <!-- Main Content -->
    <div class="mx-w-full 
        mx-10 
        p-4
        overflow-hidden 
        bg-white 
        drop-shadow-sm 
        flex flex-col space-y-6 md:space-y-0
        md:grid md:grid-cols-6 md:gap-4">

        <div class="col-span-3 2xl:col-span-2
            flex flex-col">
            
            <img class="max-w-full h-auto" src="./assets/product/img1.jpg" id="main" alt="main image">
            <div class="mt-4 flex flex-row space-x-4">
                <img class="w-28 md:w-20 lg:w-28 xl:w-24 h-auto" src="./assets/product/img2.jpg" alt="sub image">
                <img class="w-28 md:w-20 lg:w-28 xl:w-24 h-auto" src="./assets/product/img3.jpg" alt="sub image">
                <img class="w-28 md:w-20 lg:w-28 xl:w-24 h-auto" src="./assets/product/img1.jpg" alt="sub image">
                <img class="w-28 md:w-20 lg:w-28 xl:w-24 h-auto" src="./assets/product/img2.jpg" alt="sub image">
            </div>
        </div>

        <div class="col-span-3 2xl:col-span-4
            flex flex-col space-y-6">

            <h2 class="text-xl">Suitable For Apple Computer Notebook Case Cover Air Computer Case Case Case MacBookPro Case</h2>
            <h1 class="text-4xl font-bold">Rp 36,976</h1>

            <!-- Informasi Umum -->
            <div class="flex flex-col space-y-2">
                <h6 class="text-md font-semibold">Informasi Umum</h6>
    
                <div class="grid grid-cols-2">
                    <p class="col-span-1">Berat</p>
                    <p class="col-span-1">350.00 gr</p>
                </div>
                <div class="grid grid-cols-2">
                    <p class="col-span-1">Minimum Pemesanan</p>
                    <p class="col-span-1">2</p>
                </div>
                <div class="grid grid-cols-2">
                    <p class="col-span-1">Supplier</p>
                    <p class="col-span-1">德成科技实业</p>
                </div>        
            </div>

            <!-- Pilih Varian -->
            <div class="space-y-2">
                <h6 class="text-md font-semibold">Pilih Varian</h6>
                <ul class="max-w-full flex flex-row flex-wrap items-center">
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v1.jpg" alt="varian">
                    </li>
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v2.jpg" alt="varian">
                    </li>
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v3.jpg" alt="varian">
                    </li>
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v4.jpg" alt="varian">
                    </li>
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v5.jpg" alt="varian">
                    </li>
                    <li class="flex flex-wrap items-center px-1 cursor-pointer mb-3 mr-3 border-sky-200 hover:border-2 hover:border-sky-500 border-2 shadow-sm">
                        <img src="./assets/varian/v6.jpg" alt="varian">
                    </li>
                </ul> 
            </div>

            <div class="space-y-2">
                <!-- Button Keranjang -->
                <button class="bg-sky-400 hover:bg-sky-600 focus:bg-sky-600 w-full text-white font-bold py-2 rounded-md flex flex-row justify-center items-center">
                    <CartIcon class="h-6 mr-2 fill-neutral-50"/>
                    Tambahkan ke Keranjang
                </button>
                
                <!-- Button Whistlist -->
                <button class="bg-pink-400 hover:bg-pink-600 focus:bg-pink-600 w-full text-white font-bold py-2 rounded-md flex flex-row justify-center items-center">
                    <LoveIcon class="h-6 mr-2 fill-neutral-50"/>
                    Whistlist
                </button>

            </div>

            <a href="#" class="text-indigo-600">
                Lihat di 1688
            </a>
        </div>
    </div>

    <!-- Description & Summary Price -->
    <div class="mx-w-full 
        mx-10 
        my-4
        p-4
        overflow-hidden 
        bg-white 
        drop-shadow-sm 
        flex flex-col space-y-6">
    
        <TabDetail />
    </div>

    <Footer />
</template>

