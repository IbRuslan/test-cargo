<script setup>
import Button from "@/components/common/Button.vue";
import ReviewCard from "@/components/modules/ReviewCard.vue";
import SkillCard from "@/components/modules/SkillCard.vue";

const reviewItems = [
  {id: 1, title: 'Совершено перевозок', images: '/src/assets/images/icons/transportetion.svg', score: 950},
  {id: 2, title: 'Довольных клиентов', images: '/src/assets/images/icons/clients.svg', score: 1205},
  {id: 3, title: 'Членов команды', images: '/src/assets/images/icons/team.svg', score: 120},
]

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
  <div class="flex justify-center py-10">
    <div class="flex gap-28">
      <div class="flex flex-col gap-10">
        <div class="flex flex-col gap-6">
          <div>
            <h1 class="font-bold mb-8 text-lg">О компании</h1>
            <h2 class="font-bold text-4xl">Ведущий мировой<br/> бизнес</h2>
          </div>
          <div>
            <p class="text-[#6C6C6C]">
              Мы сформировали команду сотрудников, прошедших<br/> профессиональное обучение, которые готовы
              эффективно<br/>
              справляться с любыми возникающими ситуациями, обеспечивая<br/> спокойствие наших клиентов.
            </p>
          </div>
          <div>
            <div class="flex items-center gap-5 justify-center">
              <span class="font-bold text-lg border-r-2 pr-5">CEO Zhang Huawei</span>
              <img src="/src/assets/images/background/signature.png" alt="signature">
            </div>
          </div>
        </div>
        <div class="flex flex-col gap-10 py-20">
          <div class="flex flex-col gap-10">
            <div class="flex border-b-2 pb-2 mb-6">
              <div>
                <span class="font-bold text-lg border-b-4 pb-2 pr-20 border-b-blue-700 cursor-pointer">Наша цель</span>
              </div>
              <div>
                <span class="font-bold text-lg text-[#6C6C6C] pb-2 pr-20 cursor-pointer">Наше виденье</span>
              </div>
            </div>
            <div>
              <p class="text-[#6C6C6C]">Предоставляем нашим клиентам возможность осуществлять их<br/> отправления
                экологичным способом.</p>
            </div>
            <div class="mb-10 flex flex-col gap-4">
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-500 rounded"></div>
                <span class="font-bold text-lg">Высший класс услуг в области<br/> транспортировки и логистики.</span>
              </div>
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-500 rounded"></div>
                <span class="font-bold text-lg">Гарантия своевременной доставки.</span>
              </div>
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-500 rounded"></div>
                <span class="font-bold text-lg">Самые выгодные условия доставки для клиентов.</span>
              </div>
            </div>
          </div>
          <div>
            <Button>Читать дальше</Button>
          </div>
        </div>
      </div>
      <div class="py-14">
        <img src="/src/assets/images/background/cargo-container-ship.png" alt="ship">
      </div>
    </div>
  </div>

  <div class="flex justify-center mb-12 pb-10">
    <div class="flex gap-10 p-10">
      <ReviewCard v-for="item in reviewItems" :key="item.id" :images="item.images" :score="item.score"
                  :title="item.title"
      />
    </div>
  </div>

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