<script setup>
import Button from "@/components/common/Button.vue";
</script>

<template>
  <div class="w-full bg-blend-darken h-screen bg-no-repeat"
       style="background-image: url('/src/assets/images/background/delivered-directly-to-her-door.png')">
    <div class="overlay flex justify-start items-center">
      <div class="text-white ml-64 flex flex-col gap-6 w-2/5">
        <div>
          <p class="text-sm">Доставка груза: без границ и ограничений</p>
        </div>
        <div class="mb-24 flex flex-col gap-5">
          <p class="text-6xl"><b>CARGO PRO - ваш ключ к простой и быстрой логистике.</b></p>
          <p class="text-lg">Доверьте нам свои отправления, и мы гарантируем их<br/> своевременную и надежную доставку. Все ваши потребности -
            наш<br/> приоритет!</p>
        </div>
        <div><Button>Наши сервисы</Button></div>
      </div>
    </div>
  </div>
</template>


<style>
.overlay {
  top: 0;
  left: 0;
  width: 100%;
  height: 768px;
  background-color: rgb(176, 174, 174);
  mix-blend-mode: multiply;
}
</style>