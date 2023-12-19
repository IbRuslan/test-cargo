<script setup>
import Button from "@/components/common/Button.vue";
</script>


<template>
  <div class="transport-container flex w-full">
    <div class="man-on-railway"
         style="background-image: url('/src/assets/images/background/man-on-railway-track.png')">
    </div>
    <div class="transport p-20 flex flex-col gap-16 justify-center">
      <div>
        <h2 class="text-white font-bold text-5xl mb-10">Транспорт</h2>
        <p class="text-[#E7E7E7]">Услуги по транспортировке гарантируют быстрое и<br/> своевременное прохождение грузов
          через<br/> границы.</p>
      </div>
      <div class="text-white font-bold gap-5 w-96 grid grid-cols-2 items-center">
        <div class="flex gap-3 w-40">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По морю</span>
        </div>
        <div class="flex gap-3 w-40">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По воздуху</span>
        </div>
        <div class="flex gap-3 w-40">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По Ж/Д</span>
        </div>
        <div class="flex gap-3 w-40 whitespace-nowrap">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>Наземная перевозка</span>
        </div>
      </div>
      <div>
        <Button buttonClasses="flex justify-center items-center gap-3">
          <span>Больше наших сервисов</span>
          <img src="/src/assets/images/icons/subsidiary/arrow-left.svg" alt="arrow">
        </Button>
      </div>
    </div>
  </div>
</template>

<style>
.transport {
  flex-basis: 42%;
  background-color: #181818;
}

.transport-container {
  height: 703px;
}

.man-on-railway {
  flex-basis: 58%;
  height: 703px;
  background-repeat: no-repeat;
}
</style>