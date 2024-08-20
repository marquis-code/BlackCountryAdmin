<template>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 p-6">
      <div
        v-for="(item, index) in stats"
        :key="index"
        class="flex items-center justify-between rounded-lg border border-gray-200 bg-white p-4 shadow-md"
      >
        <div class="flex items-center">
          <img :src="dynamicIcons(item.icon)" :alt="item.label" class="h-10 w-10 bg-gray-100 p-2 rounded-md" />
          <div class="ml-4">
            <p class="text-2xl font-semibold text-gray-900">{{ item.value }}</p>
            <p class="text-sm text-gray-500">{{ item.label }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { dynamicIcons } from '@/utils/assets'; // assuming you have a dynamicIcons function in utils
  
  // Example stats data
  const stats = ref([
    { icon: 'total-properties', value: '0', label: 'Total Properties' },
    { icon: 'total-tenants', value: '0', label: 'Total tenants' },
    { icon: 'total-income', value: '₦0.00', label: 'Total Income' },
    { icon: 'total-rooms', value: '0', label: 'Total members' },
    { icon: 'total-rooms', value: '0', label: 'Total rooms' },
    { icon: 'total-rooms', value: '0', label: 'Available rooms' },
    { icon: 'total-rooms', value: '0', label: 'Occupied rooms' },
    { icon: 'total-rooms', value: '0%', label: 'Occupancy rate' },
    { icon: 'total-rooms', value: '0', label: 'Agents' },
    { icon: 'total-rooms', value: '0', label: 'Service providers' },
  ]);
  </script>
  
  <style scoped>
  /* Customize additional styles if necessary */
  </style>
  