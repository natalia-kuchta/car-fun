
<script setup lang="ts">
import {useUtilities} from "~/composables/useUtilities";

const route=useRoute();
const {toTitleCase} = useUtilities()

useHead({
  title:toTitleCase(route.params.name)
});

definePageMeta({
  layout:"custom",
});
</script>





<template>
  <div>

      <CarDetailHeros/>
      <CarDetailAttributes/>
      <CarDetailDescrisption/>
      <LazyCarDetailContact/>


  </div>
</template>
