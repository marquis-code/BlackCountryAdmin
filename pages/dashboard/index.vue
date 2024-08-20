<template>
  <main>
    <DashboardStats />
    <section class="flex gap-x-6">
      <div class="w-full lg:max-w-7xl space-y-6">
        <div>
          <div class="sm:block">
            <div class="">
              <nav class="-mb-px flex space-x-8" aria-label="Tabs">
                <!-- Current: "border-indigo-500 text-indigo-600", Default: "border-transparent text-gray-500 hover:border-gray-300 hover:text-gray-700" -->
                <a
                  href="#"
                  class="whitespace-nowrap border-b-4 border-[#326543] px-1 pt-4 pb-2 text-sm font-light text-[#326543]"
                  >Upcoming events</a
                >
                <a
                  href="#"
                  class="whitespace-nowrap border-b-4 border-transparent px-1 pt-4 pb-2 text-sm font-light text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  >Overdue</a
                >
                <a
                  href="#"
                  class="whitespace-nowrap border-b-4 border-transparent px-1 pt-4 pb-2 text-sm font-light text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  aria-current="page"
                  >Recent applications</a
                >
                <a
                  href="#"
                  class="whitespace-nowrap border-b-4 border-transparent px-1 pt-4 pb-2 text-sm font-light text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  >Maintenance requests</a
                >
              </nav>
            </div>
          </div>
        </div>

    <div class="space-y-5">
      <div class="overflow-hidden rounded-lg space-y-3">
        <div class="px-4 py-5 bg-white sm:px-6 flex justify-between rounded-lg items-center border [#F9FAFB] border-gray-50">
         <p>Expiring leases</p>
         <p>View all</p>
        </div>
        <div class="bg-white px-4 py-5 sm:p-6 h-80 rounded-lg flex flex-col gap-y-4 justify-center border items-center border-gray-50">
          <img
          :src="dynamicIcons('leases-empty-state')"
          alt="leases empty state"
          class=""
        />
        <p class="text-[#1D2739]">No applications to review</p>
        </div>
      </div>

      <div class="overflow-hidden rounded-lg space-y-3">
        <div class="px-4 py-5 bg-white sm:px-6 flex justify-between rounded-lg items-center border [#F9FAFB] border-gray-50">
          <p>Upcoming(Due) payment</p>
         <p>View all</p>
        </div>
        <div class="bg-white px-4 py-5 sm:p-6 h-80 rounded-lg flex flex-col gap-y-4 justify-center border items-center border-gray-50">
          <img
          :src="dynamicIcons('payment-empty-state')"
          alt="leases empty state"
          class=""
        />
        <p class="text-[#1D2739]">No applications to review</p>
        </div>
      </div>
    </div>
      </div>
      <div class="w-full lg:max-w-sm">
        <div class="overflow-hidden rounded-lg">
          <div class="py-5">
            <!-- Content goes here -->
            <p>Users activities</p>
            <!-- We use less vertical padding on card headers on desktop than on body sections -->
          </div>
          <div class="bg-white border rounded-lg border-gray-50 px-4 py-5 sm:p-6 h-80 flex flex-col gap-y-4 justify-center items-center">
            <img
            :src="dynamicIcons('activities-empty-state')"
            alt="leases empty state"
            class=""
          />
          <p class="text-[#1D2739]">No recent activities</p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
import { dynamicIcons } from "@/utils/assets";
definePageMeta({
  layout: "dashboard",
});
</script>
