<template>
    <div class="bg-white p-4 rounded-xl flex flex-col gap-y-6.5">
        <div class="flex justify-between items-center">
            <h3 class="text-[20px] font-semibold">Top Selling Product</h3>
            <NuxtLink to="/products" class="text-[15px] cursor-pointer">See All Product</NuxtLink>
        </div>
        <ul class="space-y-2">
            <li v-for="p in topProducts" :key="p.name" class="flex justify-between">
                <span>{{ p.name }}</span>
                <span class="font-medium">{{ p.quantity }}</span>
            </li>
        </ul>
    </div>
</template>

<script setup lang='ts'>
defineProps<{
    topProducts: { name: string; quantity: number }[]
}>()
</script>