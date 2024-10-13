<script setup>
import { ArrowUpRight } from 'lucide-vue-next';
</script>

<template>
    <div class="w-[calc(100vw-1px)] h-[80vh] flex gap-5 pl-8 overflow-x-scroll scrollnotvis pr-5">
        <div class="trending-main w-[500px] h-[500px] rounded-xl p-3 flex flex-col min-w-[500px]">
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
        <div class="dicover w-[500px] h-[500px] rounded-xl p-3 flex flex-col min-w-[500px]">
            <h2 class="font-inter text-[40px] font-semibold text-gayblack leading-[50px]">
                Discover the essence Minimalist furniture design & style
            </h2>
            <div class="w-full h-[230px] mt-auto">
                <div class="w-full h-10 rounded-xl flex place-items-center gap-7 [&>h2]:font-inter [&>h2]:text-[13px] [&>h2]:cursor-pointer [&>h2]:text-grayc [&>h2]:font-[500]">
                    <h2 class="!text-black">Exclusive</h2>
                    <h2>Deluxe</h2>
                    <h2>Classic</h2>
                    <h2>Modern</h2>
                </div>
                <div class="h-[calc(100%-36px)] w-full bg-white rounded-xl flex p-3">
                    <div class="h-full flex flex-col justify-between">
                        <div class="w-24 h-8 rounded-xl bg-pg flex place-items-center justify-center">
                            <h3 class="text-sm font-semibold font-inter">Exclusive</h3>
                        </div>
                        <div>
                            <h1 class="font-inter font-semibold text-[18px]">
                                Pure Space Focus Duo
                            </h1>
                            <h2 class="font-inter text-sm">
                                sleek Minimalist design for Ultimate productivity and comfort.
                            </h2>
                        </div>
                        <div class="w-8 h-8 cursor-pointer rounded-full bg-pg flex place-items-center justify-center">
                            <ArrowUpRight class="w-5 h-5"/>
                        </div>
                    </div>
                    <div class="chimg w-[200px] h-full rounded-lg">

                    </div>
                </div>
            </div>
        </div>
        <div class="fav1 w-64 h-[500px] rounded-xl min-w-64">

        </div>
        <div class="fav2 w-64 h-[500px] rounded-xl min-w-64">

        </div>
        <div class="fav3 w-64 h-[500px] rounded-xl min-w-64">

        </div>
        <div class="fav4 w-[800px] h-[500px] rounded-xl min-w-[600px]">

        </div>
    </div>
</template>

<style scoped>
.scrollnotvis{
    scrollbar-width: none;
    -ms-overflow-style: none;
}
.trending-main{
    background-image: url("../components/icons/main.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
.chimg{
    background-image: url("../components/icons/chair.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
.fav1{
    background-image: url("../components/icons/fav1.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
.fav2{
    background-image: url("../components/icons/fav2.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
.fav3{
    background-image: url("../components/icons/fav3.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
.fav4{
    background-image: url("../components/icons/fav4.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}
</style>