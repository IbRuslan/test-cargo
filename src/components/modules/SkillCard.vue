<script setup>
defineProps({
  images: String,
  title: String,
  description: String
})
</script>

<template>
  <div class="flex flex-col gap-5 w-72 p-5 bg-[#FFFEFE] hover:bg-white transition hover:-translate-y-1 hover:shadow-xl">
    <div>
      <img :src="images" alt="skill">
    </div>
    <div class="flex flex-col gap-3">
      <h3 class="font-bold text-lg">{{title}}</h3>
      <p class="text-[#6C6C6C]">{{description}}</p>
    </div>
  </div>
</template>