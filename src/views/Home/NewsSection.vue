<script setup>
const newsItem = [
  {
    id: 1,
    title: 'Стоимость перевозки контейнеров',
    description: 'Сталкиваетесь с проблемами стоимости и прогнозирования? Нужны решения?',
    image: '/src/assets/images/background/a-container-gantry-crane.png',
    type: 'Транспортировка',
    data: {day: 16, month: 'Авг.', year: 2021}
  },
  {
    id: 2,
    title: 'Управление цепочкой поставок',
    description: 'Управление цепочкой поставок - важная и незаменимая часть большинства бизнесов.',
    image: '/src/assets/images/background/containers-warehouse.png',
    type: 'Цепочки поставок',
    data: {day: 16, month: 'Авг.', year: 2021}
  },
  {
    id: 3,
    title: 'Ваши логистические проблемы',
    description: 'Глобальные цепочки поставок, на которые опирается множество розничных продавцов, нарушены на длительный срок.',
    image: '/src/assets/images/background/a-container-gantry-crane.png',
    type: 'Логистика',
    data: {day: 16, month: 'Авг.', year: 2021}
  },
]
</script>

<template>
  <div class="bg-[#F8F8F8] w-full flex justify-center py-32">
    <div>
      <div class="flex justify-between">
        <h2 class="text-4xl font-bold mb-20">Новости</h2>
        <div class="flex">
          <div class="flex items-center justify-center w-10 h-10 bg-white">
            <img src="/src/assets/images/icons/subsidiary/arrow-right.svg" alt="arrow-left">
          </div>
          <div class="flex items-center justify-center w-10 h-10 bg-blue-700 cursor-pointer">
            <img src="/src/assets/images/icons/subsidiary/arrow-left.svg" alt="arrow-right">
          </div>
        </div>
      </div>
      <div class="flex gap-10">
        <div class="flex flex-col gap-5 w-96" v-for="item in newsItem" :key="item.id">
          <div>
            <img :src="item.image" alt="news">
          </div>
          <div class="flex flex-col gap-5">
            <div class="flex justify-between">
              <div class="flex items-center gap-2">
                <img src="/src/assets/images/icons/subsidiary/folder.svg" alt="folder">
                <span class="text-[#6C6C6C]">{{ item.type }}</span>
              </div>
              <div class="border-r-2"></div>
              <div class="flex items-center gap-2 mr-5">
                <img src="/src/assets/images/icons/subsidiary/time-сircle.svg" alt="time">
                <span class="text-[#6C6C6C]">{{ item.data.day }}, {{ item.data.month }} {{ item.data.year }}</span>
              </div>
            </div>
            <div>
              <h2 class="text-2xl font-bold pr-6">{{ item.title }}</h2>
            </div>
            <div>
              <p class="text-[#6C6C6C]">{{ item.description }}</p>
            </div>
            <div>
              <a class="text-lg font-bold underline hover:text-blue-400" href="#">Читать далее</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style>

</style>