<template>
    <div class="flex flex-col gap-10 p-7">
        <HelloBar />
        <CurrentProjects />
        <div class="grid grid-cols-12 grid-rows-2 gap-10">
            <TasksForToday class="row-span-2 col-span-12 md:col-span-6"/>
            <Statistics class="row-span-1 col-span-12 md:col-span-6" />
            <ProPlan class="row-span-1 col-span-12 md:col-span-6" />
        </div>
    </div>
</template>

<script setup>
import HelloBar from '@/components/main/HelloBar.vue';
import CurrentProjects from '@/components/main/CurrentProjects.vue';
import TasksForToday from '@/components/main/TasksForToday.vue';
import Statistics from '@/components/main/Statistics.vue';
import ProPlan from '@/components/main/ProPlan.vue';
</script>