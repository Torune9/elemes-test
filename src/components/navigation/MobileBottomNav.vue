<template>
    <div class="w-full fixed flex flex-row bottom-0 justify-around text-gray-600 md:hidden bg-soft-ivory">
        <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500">
            <i class="pi pi-home" style="font-size: 2rem"></i>
            <p>Home</p>
        </button>
        <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500">
            <i class="pi pi-ticket" style="font-size: 2rem"></i>
            <p>Promotions</p>
        </button>
        <button class="cursor-pointer hover:text-gray-700 transition-colors duration-500" @click="showOtherMenu">
            <i class="pi pi-bars" style="font-size: 2rem"></i>
            <p>Other</p>
        </button>
        <!-- Other Menu -->
        <div class="absolute -translate-y-full right-0 flex flex-col gap-y-4 text-lg bg-soft-white w-40 py-2"
            v-if="isOtherMenu">
            <button class="py-2 cursor-pointer hover:bg-soft-ivory border-b">Masuk</button>
            <button class="py-2 cursor-pointer hover:bg-soft-ivory border-b">About</button>
            <button class="py-2 cursor-pointer hover:bg-soft-ivory border-b">Blogs</button>
            <button class="py-2 cursor-pointer hover:bg-soft-ivory border-b">Contact Us</button>
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