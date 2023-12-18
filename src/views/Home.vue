<script setup>
import Button from "@/components/common/Button.vue";
import SkillCard from "@/components/modules/SkillCard.vue";
import ReviewCard from "@/components/modules/ReviewCard.vue";

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

const reviewItems = [
  {id: 1, title: 'Совершено перевозок', images: '/src/assets/images/icons/transportetion.svg', score: 950},
  {id: 2, title: 'Довольных клиентов', images: '/src/assets/images/icons/clients.svg', score: 1205},
  {id: 3, title: 'Членов команды', images: '/src/assets/images/icons/team.svg', score: 120},
]
</script>

<template>
  <div class="relative w-full bg-blend-darken h-screen bg-no-repeat"
       style="background-image: url('/src/assets/images/background/delivered-directly-to-her-door.png')">
    <div class="overlay absolute top-0 left-0 w-full bg-gray-700 opacity-50"></div>
    <div class="flex justify-start items-center z-10 relative">
      <div class="ml-64 mt-28 flex flex-col gap-6 w-2/5 text-white">
        <p class="text-sm">Доставка груза: без границ и ограничений</p>
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

  <div class="flex justify-center items-center mb-28">
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

  <div class="tranport-container flex w-full">
    <div class="man-on-railway"
         style="background-image: url('/src/assets/images/background/man-on-railway-track.png')">

    </div>
    <div class="transport p-20 flex flex-col gap-16 justify-center">
      <div>
        <h2 class="text-white font-bold text-5xl mb-10">Транспорт</h2>
        <p class="text-[#E7E7E7]">Услуги по транспортировке гарантируют быстрое и<br/> своевременное прохождение грузов
          через<br/> границы.</p>
      </div>
      <div class="text-white font-bold text-lg flex gap-5 flex-wrap w-96 justify-between">
        <div class="flex gap-3">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По морю</span>
        </div>
        <div class="flex gap-3">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По воздуху</span>
        </div>
        <div class="flex gap-3">
          <img src="/src/assets/images/icons/check.svg" alt="check">
          <span>По Ж/Д</span>
        </div>
        <div class="flex gap-3">
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

  <div class="w-full flex justify-center p-32">
    <div class="flex justify-center items-center gap-32">
      <div>
        <div class="mb-20 flex flex-col gap-10">
          <h2 class="text-4xl font-bold">
            Профессионалы в<br/> траспортировке
          </h2>
          <p>
            Мы предоставляем комплексные услуги по транспортировке для<br/>
            наших партнеров по всему миру и всегда предлагаем<br/>
            инновационные решения для сложных логистических задач.
          </p>
        </div>
        <Button button-classes="px-20">О нас</Button>
      </div>
      <div class="review flex flex-col flex-wrap justify-center gap-5">
        <ReviewCard v-for="(item, index) in reviewItems" :key="item.id" :images="item.images" :score="item.score"
                    :title="item.title"
                    :style="{ flexBasis: index === 0 ? '55%' : 'auto', backgroundColor: index === 0 ? 'black' : 'auto', color: index === 0 ? 'white' : 'auto' }"
        />
      </div>
    </div>
  </div>
</template>

<style>
.overlay {
  height: 768px;
}

.logistic {
  width: 1290px;
  height: 606px;
}

.tranport-container {
  height: 703px;
}

.man-on-railway {
  flex-basis: 58%;
  height: 703px;
  background-repeat: no-repeat;
}

.transport {
  flex-basis: 42%;
  background-color: #181818;
}

.review {
  width: 602px;
  height: 504px;
}
</style>
