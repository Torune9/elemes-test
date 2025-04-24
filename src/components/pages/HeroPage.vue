<template>
    <div
        class="grid lg:grid-cols-2 lg:grid-rows-4 gap-4 lg:gap-0 py-8 px-8 h-screen relative before:absolute before:inset-0 before:w-full before:h-full before:bg-cover before:-z-1 before:bg-center before:bg-no-repeat before:opacity-2 before:bg-[url('@/assets/images/bg.png')] sm:px-24 lg:px-16">
        <!-- Header -->
        <section class="capitalize text-5xl lg:text-6xl font-[450] text-light-green">
            <h1>good food us</h1>
            <h1>good mood</h1>
        </section>
        <!-- Most Recommended -->
        <section class="relative lg:row-span-3 lg:flex justify-center items-center">
            <!-- Image Recommended -->
            <div class="flex items-center bg-soft-white/80 rounded-full p-6 w-56 h-56 lg:w-96 lg:h-96">
                <div>
                    <img :src="salad" alt="salad-image">
                </div>
            </div>
            <!-- Info Card -->
            <div
                class="absolute top-2/4 left-[15%] lg:top-3/4 lg:left-0 w-72 rounded-xl flex flex-row gap-x-4 items-center py-2 px-4 bg-white/50 backdrop-blur-sm shadow-2xl">
                <div class="w-14">
                    <img :src="salad" alt="salad-image">
                </div>
                <div class="space-y-1">
                    <h1 class="font-semibold">Green Salad Tomato</h1>
                    <p class="text-medium-gray text-sm">Tomato</p>
                    <span v-for="n in 5" class="text-orange-500 inline-block pl-1 text-xs">
                        <i class="pi pi-star-fill"></i>
                    </span>
                </div>
            </div>
        </section>
        <!-- Description -->
        <section class="lg:row-start-2 lg:py-4">
            <p class="text-medium-gray">
                I would think that conserving our natural resources should be a conservative position: Not to waste
                food, and not to throw away a lot of the food that we buy.
            </p>
        </section>
        <!-- Btn Navigation -->
        <section class="space-x-4 lg:row-start-3">
            <ButtonAction
                class="bg-primary text-white py-2 px-4 rounded-full shadow-2xl cursor-pointer hover:bg-light-green transition-colors duration-500">
                Daftar Sekarang
            </ButtonAction>
            <ButtonAction
                class="bg-soft-white py-2 px-4 rounded-full cursor-pointer hover:bg-slate-400 transition-colors duration-500">
                About Us
            </ButtonAction>
        </section>
    </div>
</template>

<script setup>
import salad from '@/assets/images/foods/salad.png'
import ButtonAction from '../ui/ButtonAction.vue';
</script>