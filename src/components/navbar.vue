<template>
    <nav class="
        mx-w-full
        px-4
        py-6
        md:flex md:justify-between md:items-center
        bg-white
        drop-shadow-md">
      
        <div class ="flex items-center justify-between">
            <div class="lg:mx-20">
            <a href="#" class="hidden lg:flex">
                <img src="../assets/logo-navbar.png" alt="caribarang.id" width="150">
            </a>
            </div>
        </div>

        <div class="
            flex 
            space-y-0 
            flex-row 
            justify-between 
            items-center 
            space-x-10 
            mt-0">

            <div>    
            </div>

            <ul class="flex flex-row space-x-10">
                <li class="text-[#3366cc]"><a href="#">Produk 1668.com</a></li>
                <li class="text-[#3366cc]"><a href="#">Produk Lokal Indonesia</a></li>
            </ul>
            
            <!-- Mobile menu button -->
            <div @click="toggleNav" class="flex md:hidden">
            <button
                type="button"
                class="
                text-[#3366cc]
                hover:text-gray-400
                focus:outline-none focus:text-gray-400
                "
            >
                <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                <path
                    fill-rule="evenodd"
                    d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
                ></path>
                </svg>
            </button>
            </div>
    </div>

      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->

    <div
        :class="showMenu ? 'flex' : 'hidden'"
        class="
          flex-col
          mt-4
          space-y-4
          md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0
          lg:mx-20
        "
      >
        <a href="#" class="bg-blue-500 hover:bg-blue-700 text-white text-center font-bold py-2 px-4 rounded">Sign In</a>
    </div>

    </nav>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    let showMenu = ref(false);
    const toggleNav = () => (showMenu.value = !showMenu.value);
    return { showMenu, toggleNav };
  },
};
</script>