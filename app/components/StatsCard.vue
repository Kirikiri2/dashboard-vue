<script setup lang="ts">
import { Icon } from '@iconify/vue';

defineProps<{
    label: string
    value: string | number
    icon: string
}>()
</script>

<template>
    <div class="w-full max-w-84">
        <div class=" hover:bg-black hover:text-white text-black bg-white p-3.5 transition-colors rounded-xl">
            <div class="flex justify-between items-center">
                <p class="text-[18px] font-semibold">
                    {{ label }}
                </p>

                <div class="p-2.5 bg-white transition-colors rounded-md">
                    <Icon :icon="icon" class="size-6.25 text-black" />
                </div>
            </div>

            <h3 class="text-[32px] font-semibold mt-6.25">{{ value }}</h3>
        </div>

    </div>
</template>