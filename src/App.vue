<script setup>
import NavBar from '@/components/navigation/NavBar.vue';
import MainContent from '@/components/main/MainContent.vue';
import Calendar from '@/components/calendar/Calendar.vue';
</script>

<template>
  <div class="grid grid-cols-12 gap-2 h-screen">
    <div class="col-span-12 xl:col-span-9 bg-stone-50 rounded-r-[37px] md:divide-x-2 flex gap-2 flex-col lg:flex-row">
      <div class="lg:w-[250px] w-full lg:h-full overflow-hidden">
        <NavBar />
      </div>
        <MainContent class="flex-1"/>
    </div>
    <div class="hidden xl:col-span-3 xl:block">
        <Calendar class="p-10"/>
    </div>
  </div>
</template>
