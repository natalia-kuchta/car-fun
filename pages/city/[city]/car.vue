
<script setup lang="ts">

const route=useRoute();
const {toTitleCase}= useUtilities()

useHead({
  title:`${route.params.make ? toTitleCase(route.params.make): 'Cars'
  } in ${toTitleCase(route.params.city)}`
});


definePageMeta({
  layout:"custom"
});



</script>


<template>
  <div>

    <div class="mt-32 flex">
      <CarSideBar/>
      <NuxtPage/>
    </div>
    </div>
</template>
