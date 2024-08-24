<script setup lang="ts">

import {navigateTo} from "#app";

const city=ref("")
const router=useRouter()
const cityError=ref(false)

const handleSearch=()=>{
  if(!city.value){
    return cityError.value=true
  }
  navigateTo(`/city/${city.value}/car`);

};

</script>

<template>
  <div
      class="font-serif w-[1000px] text-2xl rounded-full flex justify-between overflow-hidden drop-shadow-2xl mx-auto border border-pink-800"
  >
    <input
        type="text"
        class="py-3 px-5 w-full text-2xl focus:outline-none text-white bg-black/50 backdrop-blur-xl"
        :class="cityError ?  'border-pink-500 border': ''  "
        placeholder="Search by city..."
        v-model="city"
    />
    <button class="bg-pink-600 px-10 text-white" @click="handleSearch">Search</button>
  </div>
</template>

<style scoped>

</style>