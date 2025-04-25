<template>
    <div class="space-y-4 min-h-screen px-8 py-20 sm:px-24 lg:px-16">
        <!-- Header -->
        <section class="text-2xl font-[450]">
            <h1>
                Browser Our Trending
            </h1>
            <h2 class="text-light-green capitalize">
                Receipt
            </h2>
        </section>
        <!-- Receipt Category -->
        <section class="space-y-4">
            <div class="flex flex-wrap gap-4">
                <BoxReceipt v-for="(receipt, index) in receipts" :key="index"
                    :base-class="`w-full rounded-2xl items-start p-4 lg:w-64 ${receipt.color}`">
                    <div class="w-24 mb-4">
                        <img :src="receipt.image" alt="img" />
                    </div>
                    <div class="text-start">
                        <h1 class="text-2xl lg:text-xl">{{ receipt.name }}</h1>
                        <p class="text-sm capitalize text-medium-gray">{{ receipt.category }}</p>
                        <span v-for="n in 5" :key="n" :class="[
                            'inline-block pl-1 text-[10px]',
                            n <= receipt.rating ? 'text-orange-500' : 'text-gray-300'
                        ]">
                            <i class="pi pi-star-fill"></i>
                        </span>
                    </div>
                </BoxReceipt>
            </div>
            <!-- Btn All Receipt -->
            <div class="text-center">
                <ButtonAction class="bg-primary text-white">
                    ALL Receipt
                </ButtonAction>
            </div>
        </section>
    </div>
</template>

<script setup>
import cupcake from "@/assets/images/foods/cupcake_choco.png"
import pizza from "@/assets/images/foods/pizza.png"
import kebab from "@/assets/images/foods/kebab.png"
import salmon from "@/assets/images/foods/sushi.png"
import doughnut from "@/assets/images/foods/doughnut.png"
import paperoni from "@/assets/images/foods/slice_pizza.png"
import kathiKebab from "@/assets/images/foods/slicing_meat.png"
import doughUnicorn from "@/assets/images/foods/unicorn_dough.png"
import BoxReceipt from "../ui/BoxReceipt.vue"
import ButtonAction from "../ui/ButtonAction.vue"

const receipts = [
    {
        name: "Pizza Paperoni",
        category: "pizza",
        image: paperoni,
        rating: 5,
        color: "bg-soft-light-blue"
    },
    {
        name: "Pizza Meat",
        category: "pizza",
        image: pizza,
        rating: 3,
        color: "bg-soft-light-blue"
    },
    {
        name: "Doner Kebab",
        category: "kebab",
        image: kebab,
        rating: 5,
        color: "bg-soft-light-deep-blue"
    },
    {
        name: "Salmon Roll",
        category: "salmon",
        image: salmon,
        rating: 4,
        color: "bg-soft-light-maroon"
    },
    {
        name: "Cupcake Choco",
        category: "cupcake",
        image: cupcake,
        rating: 4,
        color: "bg-soft-light-green"
    },
    {
        name: "Doughnut Milk",
        category: "doughnut",
        image: doughnut,
        rating: 5,
        color: "bg-soft-ivory"
    },
    {
        name: "Doughnut Unicorn",
        category: "doughnut",
        image: doughUnicorn,
        rating: 4,
        color: "bg-soft-ivory"
    },
    {
        name: "Kathi Kebab",
        category: "kebab",
        image: kathiKebab,
        rating: 4,
        color: "bg-soft-light-deep-blue"
    },

]

</script>