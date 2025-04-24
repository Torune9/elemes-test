<template>
    <nav class="font-rubik">
        <!-- Wrapper Dekstop Navigation -->
        <div class="p-4 flex flex-row justify-around">
            <!-- Logo -->
            <div>
                <img :src="logo" alt="logo-image">
            </div>
            <!-- Menus -->
            <ul class="flex flex-row gap-x-8 items-center max-md:hidden">
                <!--Child Menu -->
                <li v-for="(menu, i) in menus" class="cursor-pointer text-gray-600 group" :key="i">
                    <p class="border-b border-transparent group-hover:border-gray-600 transition-all duration-300">
                        {{ menu.name }}
                    </p>
                </li>
            </ul>
            <!-- Auth Action -->
            <div class=" flex flex-row gap-x-6 items-center">
                <ButtonAction class="max-sm:hidden">
                    Masuk
                </ButtonAction>
                <ButtonAction class="bg-green-grass text-white hover:bg-light-green transition-colors duration-500">
                    Daftar Sekarang
                </ButtonAction>
            </div>
        </div>
        <!-- Mobile Bottom Navigation -->
        <MobileBottomNav />
    </nav>
</template>

<script setup>
import logo from '@/assets/images/logo/elemes.id.png'
import ButtonAction from '../ui/ButtonAction.vue';
import MobileBottomNav from './MobileBottomNav.vue';

const menus = [
    {
        name: 'Home',
        url: ''
    },
    {
        name: 'About',
        url: ''
    },
    {
        name: 'Promotions',
        url: ''
    },
    {
        name: 'Blogs',
        url: ''
    },
    {
        name: 'Contact Us',
        url: ''
    },
]
</script>