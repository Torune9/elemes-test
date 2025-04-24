<template>
    <div class="shrink-0 rounded-md cursor-pointer transition-all duration-300 relative hover:scale-105 before:absolute before:inset-0 before:w-full before:h-full before:bg-cover before:bg-center before:bg-no-repeat before:opacity-0 hover:before:opacity-20 before:-z-1"
        :class="['before:bg-[url(@/assets/images/bg.png)]', baseClass]">
        <slot />
    </div>
</template>

<script setup>
defineProps({
    baseClass: {
        type: String,
        default: 'p-4 flex flex-col gap-y-4', // default layout
    },
})
</script>