<script setup>
import Coach from '../components/TeamComponents/Coach.vue';
import Member from '../components/TeamComponents/Member.vue';

import { ref, onMounted } from 'vue';

const coaches = ref([]);
const members = ref([]);

onMounted(async () => {
    const response = await fetch('/data/coaches.json');
    coaches.value = await response.json();
    const response2 = await fetch('/data/members.json');
    members.value = await response2.json();
});

</script>

<template>
    
    <div class=" bg-[#111111] skew-y-[-2deg] w-[100vw] h-[27rem] absolute -z-10 top-[-6rem]"></div>
    <h1 class="font-[Saira] text-white text-center text-[8rem] font-bold">OUR TEAM</h1>

    <div class=" mt-[120px]">
        <div id="coaches" class="flex justify-center gap-[60px]">
            <Coach v-for="coach in coaches.coaches" :name="coach.name" :role="coach.role" :img="coach.img"/>
        </div>
        <div id="members" class="flex mt-6 pt-4 justify-around flex-wrap gap-x-[4rem] gap-y-16 p-[100px]">
            <Member v-for="member in members.members" :name="member.name" :role="member.role" :img="member.image"/>
        </div>
    </div>
</template>

<style>
</style>
