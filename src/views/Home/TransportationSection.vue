<script setup>
import SkillCard from "@/components/modules/SkillCard.vue";

const skillItems = [
  {
    id: 1,
    title: 'Морские перевозки',
    description: 'Мы предлагаем морские грузоперевозки из страны и в страну',
    images: '/src/assets/images/icons/shipping.svg'
  },
  {
    id: 2,
    title: 'Авиаперевозки',
    description: 'Мы являемся агентом крупных и надежных авиакомпаний с высокой частотой рейсов.',
    images: '/src/assets/images/icons/aviatrans.svg'
  },
  {
    id: 3,
    title: 'Железнодорожные перевозки',
    description: 'Безопасные, надежные и экологичные решения',
    images: '/src/assets/images/icons/railtrans.svg'
  },
  {
    id: 4,
    title: 'Автомобильные перевозки',
    description: 'Мы предоставляем высококачественные и надежные услуги по дорожной перевозке грузов.',
    images: '/src/assets/images/icons/avtotrans.svg'
  },
  {
    id: 5,
    title: 'Складские услуги',
    description: 'У нас есть возможности для эффективного управления вашей логистической цепью, на начальном этапе или на месте назначения.',
    images: '/src/assets/images/icons/warehouse.svg'
  },
  {
    id: 6,
    title: 'Таможенное оформление',
    description: 'Мы поможем вам с оформлением груза в таможне без лишних сложностей.',
    images: '/src/assets/images/icons/customs.svg'
  }
];
</script>

<template>
  <div class="flex justify-center items-center mb-18 py-20">
    <div class="logistic flex justify-center flex-wrap">
      <div class="w-2/5 basis-2/5 mr-16">
        <h2 class="font-bold text-4xl mb-10">Ведущая компания в<br/> сфере транспортировки и логистики</h2>
        <p class="text-[#6C6C6C]">Мы предоставляем высококачественные комплексные услуги и<br/> всегда учитываем
          потребности наших клиентов.</p>
      </div>
      <SkillCard v-for="item in skillItems" :key="item.id" :images="item.images" :title="item.title"
                 :description="item.description"/>
    </div>
  </div>
</template>

<style>
.logistic {
  width: 1290px;
  height: 606px;
}
</style>