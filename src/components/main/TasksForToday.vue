<template>
    <div class="space-y-7 w-full">
        <h3 class="text-3xl">
            Tasks For Today
        </h3>
        <div class="flex flex-col space-y-4"> 
            <Task 
                v-for="(task, index) in tasks"
                :key="index"
                :task="task"
            />
        </div>
    </div>
</template>

<script setup>
import Task from "@/components/main/Task.vue"

const tasks = [
    {
        name: "Mobile App",
        description: "Prepare Figma File",
        color: "color_1",
        active: true,
    },
    {
        name: "UX Wireframes",
        description: "Design UX Wireframes",
        color: "color_2",
        active: false,
    },
    {
        name: "Mobile App",
        description: "Research",
        color: "color_3",
        active: false,
    },
]
</script>