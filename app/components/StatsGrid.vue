<script setup lang="ts">
import StatsCard from './StatsCard.vue';
defineProps<{
    totalOrders: number
    avgOrderValue: number
    lifetimeValue: number
}>()
</script>

<template>
    <div class="flex items-center gap-x-3.75 justify-between">
        <StatsCard label="Avg Order Value" :value="'$' + avgOrderValue.toFixed(2)" class="metriccard"
            icon="mdi:database-outline" />
        <StatsCard label="Total Orders" :value="totalOrders" class="metriccard" icon="mdi:clipboard-outline" />
        <StatsCard label="Lifetime Value" :value="'$' + lifetimeValue.toFixed(2)" class="metriccard"
            icon="mdi:dots-circle" />
    </div>
</template>