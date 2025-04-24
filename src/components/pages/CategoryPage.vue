<template>
    <div class="space-y-4 sm:px-24 lg:px-16">
        <!-- Header -->
        <section class="text-2xl px-8 font-[450] lg:px-0">
            <h1>
                Browser Our Category
            </h1>
            <h2 class="text-light-green capitalize">
                Receipt
            </h2>
        </section>
        <!-- Receipt Category -->
        <section>
            <div ref="scrollContainer" class="flex flex-row overflow-x-scroll gap-x-2 py-4 scroll-smooth"
                style="scrollbar-width: none;">
                <BoxReceipt v-for="(receipt, index) in receipts" :key="index"
                    :base-class="`h-36 w-44 flex flex-col gap-y-4 justify-center items-center ${receipt.color}`">
                    <div class="w-10 mx-auto">
                        <img :src="receipt.icon" alt="icon" />
                    </div>
                    <div class="text-sm text-center">
                        <h1>{{ receipt.name }}</h1>
                        <p>{{ `${receipt.items} items` }}</p>
                    </div>
                </BoxReceipt>
                <BoxReceipt v-for="(receipt, index) in receipts" :key="index"
                    :base-class="`h-36 w-44 flex flex-col gap-y-4 justify-center items-center ${receipt.color}`">
                    <div class="w-10 mx-auto">
                        <img :src="receipt.icon" alt="icon" />
                    </div>
                    <div class="text-sm text-center">
                        <h1>{{ receipt.name }}</h1>
                        <p>{{ `${receipt.items} items` }}</p>
                    </div>
                </BoxReceipt>
            </div>

            <div class="flex justify-end gap-x-4">
                <ButtonAction class="flex flex-row bg-primary w-32 justify-around" @click="scrollLeft">
                    <span class="text-primary rounded-full w-9 h-9 flex justify-center items-center bg-white text-3xl">
                        <i class="pi pi-angle-left"></i>
                    </span>
                    <span class="flex justify-center items-center uppercase text-white">prev</span>
                </ButtonAction>
                <ButtonAction class="flex flex-row bg-primary w-32 justify-around" @click="scrollRight">
                    <span class="flex justify-center items-center uppercase text-white">next</span>
                    <span class="text-primary rounded-full w-9 h-9 flex justify-center items-center bg-white text-3xl">
                        <i class="pi pi-angle-right"></i>
                    </span>
                </ButtonAction>
            </div>
        </section>
    </div>
</template>

<script setup>
import cupcake from "@/assets/icons/cupcake.svg"
import pizza from "@/assets/icons/pizza.svg"
import kebab from "@/assets/icons/kebab.svg"
import salmon from "@/assets/icons/salmon.svg"
import doughnut from "@/assets/icons/doughnut.svg"
import ButtonAction from "../ui/ButtonAction.vue"

import { ref } from 'vue'
import BoxReceipt from "../ui/BoxReceipt.vue"

const receipts = [
    {
        name: "Cupcake",
        icon: cupcake,
        items: 22,
        color: "bg-soft-light-green"
    },
    {
        name: "Pizza",
        icon: pizza,
        items: 25,
        color: "bg-soft-light-blue"
    },
    {
        name: "Kebab",
        icon: kebab,
        items: 12,
        color: "bg-soft-light-deep-blue"
    },
    {
        name: "Salmon",
        icon: salmon,
        items: 22,
        color: "bg-soft-light-maroon"
    },
    {
        name: "Doughnut",
        icon: doughnut,
        items: 11,
        color: "bg-soft-ivory"
    }
]

const scrollContainer = ref(null)

const scrollLeft = () => {
    if (scrollContainer.value) {
        scrollContainer.value.scrollBy({ left: -200, behavior: 'smooth' })
    }
}

const scrollRight = () => {
    if (scrollContainer.value) {
        scrollContainer.value.scrollBy({ left: 200, behavior: 'smooth' })
    }
}


</script>