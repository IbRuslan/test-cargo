<script setup>
import SkillCard from "@/components/modules/SkillCard.vue";

const skillItems = [
  {
    id: 1,
    title: 'Конкурентные тарифы',
    description: 'Предлагаем низкую стоимость услуг в области транспортировки и логистики.',
    images: '/src/assets/images/icons/rates.svg'
  },
  {
    id: 2,
    title: 'Всегда вовремя',
    description: 'Гарантируем своевременную доставку для всех наших клиентов.',
    images: '/src/assets/images/icons/timer.svg'
  },
  {
    id: 3,
    title: 'Передовые технологии',
    description: 'Повышаем нашу эффективность с помощью современной технологии.',
    images: '/src/assets/images/icons/technologies.svg'
  },
  {
    id: 4,
    title: 'Быстро и надежно',
    description: 'Обязательное требование для логистических компаний.',
    images: '/src/assets/images/icons/fast.svg'
  },
  {
    id: 5,
    title: 'Поддержка 24/7',
    description: 'Мы готовы ответить на все ваши вопросы в любое время.',
    images: '/src/assets/images/icons/support.svg'
  },
  {
    id: 6,
    title: 'Безопасная упаковка',
    description: 'Обеспечиваем безопасность груза благодаря нашей тщательной упаковке.',
    images: '/src/assets/images/icons/safely.svg'
  }
];
</script>

<template>
  <div class="flex justify-center items-center py-32 bg-[#F8F8F8]">
    <div class="logistic flex justify-center flex-wrap gap-3">
      <div class="w-2/5 basis-2/5 mr-16 flex flex-col justify-center">
        <h2 class="font-bold text-4xl mb-10">Наше преимущество</h2>
        <p class="text-[#6C6C6C]">Наши сильные стороны и преимущества выделяют нас среди<br/> конкурентов, удовлетворяя
          все требования наших клиентов:</p>
      </div>
      <SkillCard v-for="item in skillItems" :key="item.id" :images="item.images" :title="item.title"
                 :description="item.description"/>
    </div>
  </div>
</template>
