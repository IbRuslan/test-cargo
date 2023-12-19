<script setup>
import ReviewCard from "@/components/modules/ReviewCard.vue";
import AdvantageSection from "@/views/about/AdvantageSection.vue";
import AboutCompanySection from "@/views/about/AboutCompanySection.vue";

const reviewItems = [
  {id: 1, title: 'Совершено перевозок', images: '/src/assets/images/icons/transportetion.svg', score: 950},
  {id: 2, title: 'Довольных клиентов', images: '/src/assets/images/icons/clients.svg', score: 1205},
  {id: 3, title: 'Членов команды', images: '/src/assets/images/icons/team.svg', score: 120},
]
</script>

<template>
  <AboutCompanySection/>
  <div class="flex justify-center mb-12 pb-10">
    <div class="flex gap-10 p-10">
      <ReviewCard v-for="item in reviewItems" :key="item.id" :images="item.images" :score="item.score"
                  :title="item.title"
      />
    </div>
  </div>
  <AdvantageSection/>
  <div class="bg-video w-full flex justify-center items-center" style="background-image: url('/src/assets/images/background/cargo-vessel-in-the-sea.png')">
    <div class="bg-blue-800 rounded-full p-5 pl-6 flex items-center justify-center cursor-pointer">
      <img src="/src/assets/images/icons/subsidiary/plus.svg" alt="plus">
    </div>
  </div>
</template>

<style>
.bg-video {
  height: 653px;
}
</style>