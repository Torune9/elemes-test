<template>
    <div class="fixed bottom-0 w-full">
        <div class="w-full flex flex-row justify-around text-medium-gray lg:hidden bg-soft-white py-2">
            <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500">
                <i class="pi pi-home" style="font-size: 2rem"></i>
                <p>Home</p>
            </button>
            <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500 relative">
                <i class="pi pi-ticket" style="font-size: 2rem"></i>
                <p>Promotions</p>
                <span class="absolute top-0 bg-red-600 text-white text-xs rounded-xl px-2">
                    HOT
                </span>
            </button>
            <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500" @click="showOtherMenu">
                <i class="pi pi-bars" style="font-size: 2rem"></i>
                <p>Other</p>
            </button>
            <!-- Other Menu -->
            <div class="absolute -translate-y-full right-0 flex flex-col  text-lg bg-soft-white w-40"
                v-if="isOtherMenu">
                <button
                    class="py-2 cursor-pointer hover:bg-slate-400 hover:text-white transition-colors duration-300 border-b">Masuk</button>
                <button
                    class="py-2 cursor-pointer hover:bg-slate-400 hover:text-white transition-colors duration-300 border-b">About</button>
                <button
                    class="py-2 cursor-pointer hover:bg-slate-400 hover:text-white transition-colors duration-300 border-b">Blogs</button>
                <button
                    class="py-2 cursor-pointer hover:bg-slate-400 hover:text-white transition-colors duration-300 border-b">Contact
                    Us</button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const isOtherMenu = ref(false)

const showOtherMenu = () => {
    isOtherMenu.value = !isOtherMenu.value
}
</script>