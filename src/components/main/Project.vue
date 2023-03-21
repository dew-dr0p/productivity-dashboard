<template>
    <div 
        class="rounded-xl text-white p-4 flex justify-between flex-col gap-7 bg-color_1"
        :class="`bg-${project.color}`"
    >
        <div class="flex justify-between items-center">
            <div class="flex -space-x-2">
                <img 
                    v-for="(image, index) in images"
                    :key="index"
                    :src="image" 
                    alt="person"
                    class="inline-block h-8 rounded-full ring-2"
                    :class="`ring-${project.color}`"
                />

                <button
                    class="bg-black flex justify-center items-center rounded-full w-8 h-8"
                >
                    <span class="text-sm">
                        + {{ project.people }}
                    </span>
                </button>
            </div>
            <button>
                <mdicon name="dots-vertical" />
            </button>
        </div>



        <h3 class="font-bold text-3xl">
            {{ project.name }}
        </h3>

        <div class="space-y-2">

            <p class="text-white">
                <span>{{ project.tasks }} tasks</span> |
                <span>{{ project.tasks }} tasks %</span> 
            </p>

            <div class="relative h-2 bg-black bg-opacity-20 rounded-xl">
                <span 
                    class="absolute bg-gray-200 h-2 top-0 left-0 rounded-xl"
                    :style="`width: ${project.percentage}%`"
                ></span>
            </div>

        </div>

    </div>    
</template>

<script setup>

defineProps({
    project: {
        type: Object,
        required: true
    }
})

const images = [
    "@\assets\photo_2020-07-09_11-42-40.jpg",
    "@\assets\photo_2020-07-09_11-42-40.jpg"
];
</script>