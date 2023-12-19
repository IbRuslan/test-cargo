<script setup>
import Button from "@/components/common/Button.vue";
import TransportationSection from "@/views/Home/TransportationSection.vue";
import TransportSection from "@/views/Home/TransportSection.vue";
import StatisticsSection from "@/views/Home/StatisticsSection.vue";
import NewsSection from "@/views/Home/NewsSection.vue";
import ContactsSection from "@/views/Home/ContactsSection.vue";
</script>

<template>
  <div class="back relative w-full bg-blend-darken bg-no-repeat mb-20">
    <div class="flex justify-start items-center z-10 relative">
      <div class="ml-64 mt-28 flex flex-col gap-6 w-2/5 text-white">
        <div>
          <p class="text-sm py-1">Доставка груза: без границ и ограничений</p>
          <div class="w-52 border-t border-blue-700"></div>
        </div>
        <div class="mb-24 flex flex-col gap-5">
          <p class="text-6xl"><b>CARGO PRO - ваш ключ к простой и быстрой логистике.</b></p>
          <p class="text-lg">Доверьте нам свои отправления, и мы гарантируем их своевременную и надежную доставку. Все
            ваши потребности - наш приоритет!</p>
        </div>
        <div>
          <Button>Наши сервисы</Button>
        </div>
      </div>
    </div>
  </div>
  <TransportationSection/>
  <TransportSection/>
  <StatisticsSection />
  <NewsSection/>
  <ContactsSection/>
</template>

<style>
.back {
  background-image: url("/src/assets/images/background/delivered-directly-to-her-door.png");
  background-color: rgba(82, 82, 82, 0.5); /* Измените значение альфа-канала (0.5) для настройки уровня затемнения */
  background-blend-mode: multiply;
  height: 768px;
}
</style>
