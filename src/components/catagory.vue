<script setup>
import { ref } from 'vue';

let catagories_list = ref([
    {
        name: 'Machinery',
        active: true
    },
    {
        name: 'Electronics',
    },
    {
        name: 'Furniture',
    },
    {
        name: 'Clothing',
    },
    {
        name: 'Books',
    },
    {
        name: 'Toys',
    },
    {
        name: 'Tools',
    },
    {
        name: 'Vehicles',
    },
    {
        name: 'Jewelry',
    },
    {
        name: 'Miscellaneous',
    },
    {
        name: 'Tools',
    },
    {
        name: 'Vehicles',
    },
    {
        name: 'Jewelry',
    },
    {
        name: 'Miscellaneous',
    },

])
let tags = ref([
    "All",
    "Brand New",
    "Used",
    "Refurbished",
    "Fast Delivery",
])
let activeTag = ref(["All"])
</script>

<template>
    <div class="w-full h-96 flex flex-col px-8 gap-5">
        <h1 class="text-[40px] font-bold text-gayblack">
            Catagory / Machinery
        </h1>
        <div class="w-[calc(100vw-1px)] overflow-x-auto flex gap-3 noscrollbar pr-16">
            <div v-for="(cat,catindex) in catagories_list" :key="catindex" :class="{'bg-pg': cat.active}" class="bg-white h-24 px-16 flex place-items-center rounded-xl">
                <h1 class="text-lg font-inter">
                    {{cat.name}}
                </h1>
            </div>
        </div>
        <div class="tags flex place-items-center gap-3">
            <h1 class="cursor-pointer text-nowrap text-center px-5 rounded-lg" :class="{'bg-white': activeTag.includes(tag)}" v-for="(tag,tagindex) in tags" :key="tagindex">{{tag}}</h1>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.noscrollbar{
    scrollbar-width: none;
    -ms-overflow-style: none;
    &::-webkit-scrollbar {
        display: none;
    }
}
</style>