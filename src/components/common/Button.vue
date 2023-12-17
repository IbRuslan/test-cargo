<script setup>
defineProps({
  buttonClasses: String,
  handleClick: Function
})
</script>

<template>
  <button :class="buttonClasses" class="bg-[#5367CE] py-2 px-7 text-white rounded-md text-lg cursor-pointer hover:bg-[#455DDD] active:bg-[#3350E8]" @click="handleClick">
    <slot></slot>
  </button>
</template>