<script setup>
const props = defineProps(['name', 'role', 'img'])

</script>

<template>
    <div class="bg-[#281616] outline outline-2 outline-[#EF1F13] w-[800px] h-[520px] rounded-[50px] overflow-hidden font-[Saira] text-[24px] z-10">
        <div class="flex justify-between h-[360px]">
             <img :src="props.img" class="w-[400px] h-[520px] absolute -z-10 rounded-l-[50px]">
             <div class="bg-[#ffffff00] w-[400px] h-[520px]"></div>
             <p class="w-[400px] pl-6 pr-6 pt-16 bg-[#1111118a] text-[2rem] font-bold">{{ props.role }}</p>
         </div>
         <div class="pl-[20px] pt-4 w-[800px] h-[160px] bg-[#1111118a]">
             <h2 class="text-[3rem] font-bold">{{ props.name }} </h2>
             <p class="pl-4 text-[36px]">Coach</p>
         </div>
    </div>
</template>