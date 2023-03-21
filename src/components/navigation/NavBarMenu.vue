<template>
    <ul>
        <li 
            class="p-3 flex justify-start items-center gap-3 cursor-pointer"
            :class="{
                'font-bold bg-gradient-to-tl to-pink-200 from-orange-300 rounded-xl text-gray-500': active === index
            }"
            v-for="({text, icon}, index) in items"
            :key="index"
            @click="setActive(index)"
        >
            <mdicon :name="icon" class="text-current" />
            <span>{{ text }}</span>
        </li>
    </ul>
</template>

<script setup>
import { ref } from "@vue/reactivity"

const active = ref(0);

const setActive = (index) => active.value = index

const items = [
    {text: "Dashboard", icon: "home"},
    {text: "Analytics", icon: "chart-arc"},
    {text: "Tracking", icon: "format-list-checks"},
    {text: "Setting", icon: "cog"},
]

</script>