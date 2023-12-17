<script setup>
import SkillCard from "@/components/modules/SkillCard.vue";
import ReviewCard from "@/components/modules/ReviewCard.vue";
</script>

<template>
  <div>
    <SkillCard images="/src/assets/images/icons/shipping.svg"
               title="Морские перевозки"
               description="Мы предлагаем морские грузоперевозки из страны и в страну"
    />
    <SkillCard images="/src/assets/images/icons/shipping.svg"
               title="Морские перевозки"
               description="Мы предлагаем морские грузоперевозки из страны и в страну"
    />
    <ReviewCard images="/src/assets/images/icons/clients.svg" :score="1250" title="Довольных клиентов" />
  </div>
</template>
