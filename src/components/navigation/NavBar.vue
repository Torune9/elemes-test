<template>
    <nav class="font-rubik sticky top-0 z-50 bg-white py-4">
        <!-- Wrapper Dekstop Navigation -->
        <div class="p-4 flex flex-row justify-around">
            <!-- Logo -->
            <div>
                <img :src="logo" alt="logo-image">
            </div>
            <!-- Menus -->
            <ul class="flex flex-row gap-x-8 items-center max-lg:hidden">
                <!--Child Menu -->
                <li v-for="(menu, i) in menus"
                    class="cursor-pointer text-gray-600 group hover:bg-soft-white transition-colors duration-500 p-1 relative"
                    :key="i">
                    <p>
                        {{ menu.name }}
                    </p>
                    <span v-if="menu.name == 'Promotions'"
                        class="absolute border top-0 left-3/4 -translate-y-3/5 inline-block w-12 text-center rounded-xl text-xs bg-red-600 text-white py-1">HOT</span>
                </li>
            </ul>
            <!-- Auth Action -->
            <div class=" flex flex-row gap-x-6 items-center">
                <ButtonAction class="max-sm:hidden hover:bg-soft-white transition-colors duration-500">
                    Masuk
                </ButtonAction>
                <ButtonAction class="bg-primary text-white hover:bg-light-green transition-colors duration-500">
                    Daftar Sekarang
                </ButtonAction>
            </div>
        </div>
    </nav>
</template>

<script setup>
import logo from '@/assets/images/logo/elemes.id.png'
import ButtonAction from '../ui/ButtonAction.vue';

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