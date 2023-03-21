<template>
    <div class="flex flex-col md:flex-row gap-10 justify-between items-center">
        <div class="space-y-2">
            <h1 class="font-extrabold text-5xl text-blueGray-700">Hello, Sara</h1>
            <p>
                Today is Friday, 15 April 2022
            </p>
        </div>

        <div class="flex justify-between gap-2 items-center">
            <input name="search" type="search" placeholder="">
            <button class="bg-gray-200 p-2 rounded-lg text-blueGray-500">
                <mdicon name="magnify" />
            </button>
            <button class="bg-black py-2 px-4 text-gray-300 rounded-lg hover:shadow-2xl cursor-pointer">
                Add new Project
            </button>
        </div>
    </div>
</template>