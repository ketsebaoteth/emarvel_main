<script setup>
import { ArrowUpRight } from 'lucide-vue-next';
</script>

<template>
    <div class="w-screen h-[80vh] flex gap-5 pl-5">
        <div class="trending-main w-[500px] h-[500px] rounded-xl p-3 flex flex-col">
            <div class="tags flex gap-2">
                <div class="w-24 h-8 rounded-xl bg-white flex place-items-center justify-center">
                    <h3 class="text-sm font-semibold font-inter">Exclusive</h3>
                </div>
            </div>
            <div class="disc mt-auto flex flex-col gap-2">
                <h1 class="text-[40px] font-[900] font-inter text-white leading-8">Japanese Indoor Chair</h1>
                <p class="text-[14px] font-inter text-white">Elegant Chair With Soft Surface For Comfort</p>
                <div class="flex">
                    <div class="w-32 h-8 rounded-2xl bg-white flex place-items-center justify-center cursor-pointer">
                        <h3 class="text-sm font-semibold font-inter">View Product</h3>
                    </div>
                    <div class="w-8 h-8 cursor-pointer rounded-full bg-white flex place-items-center justify-center">
                        <ArrowUpRight class="w-5 h-5"/>
                    </div>
                </div>
                
            </div>
        </div>
        <div class="dicover w-[500px] h-[500px] rounded-xl p-3 flex flex-col">
            <h2 class="font-inter text-[40px] font-semibold text-gayblack leading-[50px]">
                Discover the essence Minimalist furniture design & style
            </h2>
        </div>
    </div>
</template>

<style scoped>
.trending-main{
    background-image: url("../components/icons/main.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

</style>