<script setup>
import {
  Select,
  SelectContent,
  SelectGroup,
  SelectItem,
  SelectLabel,
  SelectTrigger,
  SelectValue,
} from '@/components/ui/select'
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuLabel,
  DropdownMenuSeparator,
  DropdownMenuTrigger,
} from '@/components/ui/dropdown-menu'

import { Bookmark, ShoppingCart, ChevronDown, Search } from 'lucide-vue-next';

import Button from './ui/button/Button.vue';
import { onMounted, ref } from 'vue';

const cartbadge = ref(null);
const carticon = ref(null);
const undersearchCont = ref(null);
const undersearch = ref(null);
const searchbar = ref(null);

function updateBadgeLocation() {
  cartbadge.value.style.top = `${carticon.value.getBoundingClientRect().top + 13}px`;
  cartbadge.value.style.left = `${carticon.value.getBoundingClientRect().left + 12}px`;
}
let searchNotOpen = true;

function updateSearch(){
  searchNotOpen = !searchNotOpen;
  undersearch_POS();
}
function undersearch_POS(){
  if(searchNotOpen){
    let undersearchEL = undersearch.value;
    undersearchEL.style.opacity = "0";
    undersearchEL.style.left = undersearchCont.value.getBoundingClientRect().left + "px";
    undersearchEL.style.top = undersearchCont.value.getBoundingClientRect().top + "px";
    undersearchEL.style.width = undersearchCont.value.getBoundingClientRect().width + "px";
    undersearchEL.style.height = undersearchCont.value.getBoundingClientRect().height + "px";
    undersearchEL.style.pointerEvents = "none";
    undersearchCont.value.style.transform = "translateY(0)";
  }else{
    let undersearchEL = undersearch.value;
    undersearchEL.style.opacity = "1";
    undersearchEL.style.left = undersearchCont.value.getBoundingClientRect().left - 15 + "px";
    undersearchEL.style.top = undersearchCont.value.getBoundingClientRect().top + "px";
    undersearchEL.style.width = undersearchCont.value.getBoundingClientRect().width+30 + "px";
    undersearchEL.style.height = "300px";
    undersearchEL.style.pointerEvents = "auto";
    undersearchCont.value.style.transform = "translateY(5px)";
  }
}
onMounted(() => {
  updateBadgeLocation();
  undersearch_POS();
  window.addEventListener("resize", updateBadgeLocation);
})

</script>

<template>
    <div class="w-full h-28 flex place-items-center px-16 gap-8">
        <h1 class="font-inter font-[800] text-[24px]">EMARVEL</h1>
        <div ref="cartbadge" class="w-4 h-4 bg-[#b9ddff] absolute rounded-full flex place-items-center justify-center">
          <h1 class="text-[12px] font-bold">3</h1>
        </div>
        <div ref="undersearch" class=" absolute under_search bg-white z-10 rounded-xl">

        </div>
        <Select >
            <SelectTrigger class="w-[75px] bg-transparent ring-0 border-0 focus-visible:ring-offset-0 focus-visible:ring-0" >
              <SelectValue placeholder="ETB" class="font-inter text-grayc outline-none ring-0 focus:ring-0" />
            </SelectTrigger>
            <SelectContent>
              <SelectGroup>
                <SelectLabel>Currency</SelectLabel>
                <SelectItem value="etb">
                  ETB
                </SelectItem>
                <SelectItem value="dollars">
                  USD
                </SelectItem>
                <SelectItem value="euro">
                  EUR
                </SelectItem>
                <SelectItem value="shiling">
                  GBP
                </SelectItem>
                <SelectItem value="yun">
                  JPY
                </SelectItem>
              </SelectGroup>
            </SelectContent>
        </Select>
        <div ref="undersearchCont" class=" undersearchCont flex gap-2 flex-grow z-20">
          <div ref="searchbar" style="gap: 4px;" class="searcharea flex place-items-center bg-white ml-auto pl-0 pr-5 rounded-xl w-[100%]">
            <Search class="absolute ml-3 w-5"/>
            <input type="text" @focus="updateSearch" @blur="updateSearch" class="w-full h-12 rounded-xl ml-auto outline-none px-10 pl-12 placeholder:text-grayc font-inter text-sm" placeholder="Search For Products">
            <h2 class="shortcut text-nowrap flex place-items-center gap-1 text-grayc font-inter text-sm"><span class="text-[13px] text-grayc font-semibold">⌘</span> CTRL+S</h2>
          </div>
          <Button class="bg-white text-black h-[52px] rounded-xl w-24 font-inter border-0" variant="outline">Search</Button>
        </div>
        <div class="flex gap-5">
          <Bookmark class="ml-auto min-w-5"/>
          <ShoppingCart ref="carticon" class="min-w-5" />
        </div>

        <div class="w-36 h-full flex place-items-center gap-4">
          <img src="../components/icons/Ladies Profile Picture 1.png" alt="" class="h-14">
          <div class="textsection flex flex-col w-full">
            <h6 class="text-[13px]">Hi Lisa</h6>

            <DropdownMenu>
              <DropdownMenuTrigger>
                <button class="flex place-items-center gap-1">
                  <p class="text-[13px
                  ] text-nowrap font-bold">Lisa Jhonson</p>
                  <ChevronDown class="w-4 h-4" />
                </button>
              </DropdownMenuTrigger>
              <DropdownMenuContent class="w-64 mt-2 mr-3">
                <DropdownMenuItem>
                  <DropdownMenuLabel>Profile</DropdownMenuLabel>
                </DropdownMenuItem>
                <DropdownMenuItem>
                  <DropdownMenuLabel>Settings</DropdownMenuLabel>
                </DropdownMenuItem>
                <DropdownMenuSeparator />
                <DropdownMenuItem>
                  <DropdownMenuLabel>Logout</DropdownMenuLabel>
                </DropdownMenuItem>
              </DropdownMenuContent>
            </DropdownMenu>

          </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.under_search{
  transition: 0.5s cubic-bezier(0.18, 0.89, 0.32, 1.28);
}
.undersearchCont{
  transition: 0.5s cubic-bezier(0.18, 0.89, 0.32, 1.28);
}
</style>