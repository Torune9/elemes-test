<template>
    <footer>
        <div
            class="grid grid-cols-2 lg:grid-cols-5 grid-flow-row bg-secondary font-rubik px-8 gap-2 py-28 sm:px-24 lg:px-16 lg:py-10">
            <!-- Main Info -->
            <div class="col-span-2 space-y-4">
                <!-- Logo -->
                <div>
                    <img :src="logo" alt="">
                </div>
                <!-- Address -->
                <p class="text-medium-gray max-w-96">
                    Jl. Prof. DR. Satrio No.7, RT.3/RW.3, Karet Kuningan,
                    Kecamatan Setiabudi, Kota Jakarta Selatan,
                    Daerah Khusus Ibukota Jakarta 12950
                </p>
                <!-- Contact -->
                <div class="flex flex-row gap-x-2">
                    <ButtonAction
                        class="bg-white hover:bg-primary transition-colors duration-500 hover:text-white p-1 h-10 w-10 flex justify-center items-center">
                        <i class="pi pi-envelope"></i>
                    </ButtonAction>
                    <ButtonAction
                        class="bg-white hover:bg-primary transition-colors duration-500 hover:text-white p-1 h-10 w-10 flex justify-center items-center">
                        <i class="pi pi-phone"></i>
                    </ButtonAction>
                    <ButtonAction
                        class="bg-white hover:bg-primary transition-colors duration-500 hover:text-white p-1 h-10 w-10 flex justify-center items-center">
                        <i class="pi pi-instagram"></i>
                    </ButtonAction>
                </div>
            </div>
            <!-- Category -->
            <div class="space-y-4">
                <h1 class="font-semibold">Categories</h1>
                <ul class="text-medium-gray space-y-2">
                    <li v-for="category in categories" class="hover:border-b w-fit cursor-pointer">
                        {{ category.name }}
                    </li>
                </ul>
            </div>
            <!-- About Us -->
            <div class="space-y-4">
                <h1 class="font-semibold">About Us</h1>
                <ul class="text-medium-gray space-y-2">
                    <li v-for="about in about" class="hover:border-b w-fit cursor-pointer">
                        {{ about.name }}
                    </li>
                </ul>
            </div>
            <!-- News Letter -->
            <div class="col-span-2 lg:col-span-1 space-y-4">
                <h1 class="font-semibold">
                    News Letter
                </h1>
                <div class="space-y-4">
                    <p class="text-medium-gray">
                        Get now free 50% discount for alll products on your first order
                    </p>
                    <div class="flex flex-row">
                        <input type="text" class="border p-2 border-r-0 rounded-tl-md rounded-bl-md lg:w-40"
                            placeholder="Your email address" />
                        <button class="bg-primary w-16 rounded-br-md rounded-tr-md uppercase text-white">Send</button>
                    </div>
                    <div class="space-y-4">
                        <div class="space-x-2">
                            <i class="pi pi-envelope"></i>
                            <span>elemesid@gmail.com</span>
                        </div>
                        <div class="space-x-2">
                            <i class="pi pi-phone"></i>
                            <span>0888 1111 2222</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script setup>
import logo from '@/assets/images/logo/elemes.id.png'
import ButtonAction from '../ui/ButtonAction.vue';
const categories = [
    {
        name: "Cupcake",
    },
    {
        name: "Pizza",
    },
    {
        name: "Kebab",
    },
    {
        name: "Salmon",
    },
    {
        name: "Doughnut",
    }
]

const about = [
    {
        name: "About Us",
    },
    {
        name: "FAQ",
    },
    {
        name: "Report Problem",
    },
]
</script>