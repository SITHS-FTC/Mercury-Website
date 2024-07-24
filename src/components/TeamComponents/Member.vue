<script setup>
const props = defineProps(['name', 'role', 'img'])

</script>

<template>
    <div class="bg-[#281616] outline outline-2 outline-[#EF1F13] w-[300px] h-[400px] rounded-[50px] overflow-hidden font-[Saira] text-[24px] z-10">
        <div class="flex justify-between">
             <img :src="props.img" class="w-[300px] h-[400px] absolute -z-10 rounded-[50px]">
             <div class="bg-[#ffffff00] w-[300px] h-[300px]"></div>
         </div>
         <div class="pl-[20px] w-[600px] h-[100px] bg-[#1111118a]">
             <h2 class="text-[32px] font-bold">{{ props.name }}</h2>
             <p class="pl-4">{{ props.role }}</p>
         </div>
    </div>
</template>