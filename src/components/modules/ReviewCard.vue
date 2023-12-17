<script setup>
defineProps({
  images: String,
  score: Number,
  title: String
})
</script>

<template>
  <div class="p-10 rounded-lg w-72 h-52 flex justify-center items-center shadow-xl">
    <div class="flex flex-col gap-4 text-center">
      <div class="flex items-center gap-2">
        <img :src="images" alt="review">
        <b class="font-bold text-5xl">{{score}}</b>
      </div>
      <div>
        <p class="text-[#6C6C6C]">{{title}}</p>
      </div>
    </div>
  </div>
</template>