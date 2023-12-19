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

  <div class="w-full flex justify-center p-32">
    <div class="flex justify-center items-center gap-32">
      <div>
        <div class="mb-20 flex flex-col gap-10">
          <h2 class="text-5xl font-bold">
            Профессионалы в<br/> траспортировке
          </h2>
          <p>
            Мы предоставляем комплексные услуги по транспортировке для<br/>
            наших партнеров по всему миру и всегда предлагаем<br/>
            инновационные решения для сложных логистических задач.
          </p>
        </div>
        <Button buttonClasses="px-20">О нас</Button>
      </div>
      <div class="review flex flex-col flex-wrap justify-center gap-5">
        <ReviewCard v-for="(item, index) in reviewItems" :key="item.id" :images="item.images" :score="item.score"
                    :title="item.title"
                    :style="{ flexBasis: index === 0 ? '55%' : 'auto', backgroundColor: index === 0 ? 'black' : 'auto', color: index === 0 ? 'white' : 'auto' }"
        />
      </div>
    </div>
  </div>

  <div class="w-full flex justify-center p-32">
    <div>
      <h2 class="text-5xl font-bold mb-20">Наши Процессы</h2>
      <div>
        <div class="w-full flex gap-36 mb-10 border-b-2 pb-4">
          <div>
            <span class="cursor-pointer font-bold text-xl mr-10 border-b-2 pb-4 border-b-blue-700">Перед отправкой</span>
          </div>
          <div>
            <span class="cursor-pointer text-[#6C6C6C] text-xl mr-10">Во время отправки</span>
          </div>
          <div>
            <span class="cursor-pointer text-[#6C6C6C] text-xl mr-10">После отправки</span>
          </div>
        </div>
        <div class="flex gap-16 justify-center items-center">
          <div class="flex flex-col gap-10">
            <p class="text-[#6C6C6C]">
              Мы гарантируем строгое соблюдение всех<br/> процедур до, во время и после перевозки.
            </p>
            <div class="mb-10 flex flex-col gap-6">
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-700 rotate-45"></div>
                <span class="font-bold text-lg">Стандартные операционные процедуры по<br/> обслуживанию транспортных средств</span>
              </div>
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-700 rotate-45"></div>
                <span class="font-bold text-lg">План управления транспортировкой</span>
              </div>
              <div class="flex items-center gap-3">
                <div class="w-2 h-2 bg-blue-700 rotate-45"></div>
                <span class="font-bold text-lg">Стандартные операционные процедуры для погрузки.</span>
              </div>
            </div>
            <div>
              <Button>Посмотреть детали</Button>
            </div>
          </div>
          <div>
            <img src="/src/assets/images/background/young-warehouse-workers-working.png" alt="work">
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="bg-[#F8F8F8] w-full flex justify-center p-32">
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

  <div class="w-full flex justify-center p-40">
    <div class="flex gap-36">
      <div class="flex flex-col gap-14">
        <div class="flex flex-col gap-8">
          <h2 class="text-4xl font-bold">Оставайтесь на связи</h2>
          <p class="text-[#6C6C6C]">Свяжитесь с нами напрямую по телефону или заполните форму,<br/> чтобы получить бесплатную консультацию от нашего
            персонала.</p>
        </div>
        <div class="flex flex-col gap-5">
          <div class="flex flex-col gap-2">
            <div class="flex gap-3">
              <img src="/src/assets/images/icons/contacts/phone.svg" alt="phone">
              <span class="text-[#6C6C6C]">Номер телефона</span>
            </div>
            <div>
              <span class="text-2xl font-bold">+7 (495) 885 71 35</span>
            </div>
          </div>
          <div class="flex flex-col gap-2">
            <div class="flex gap-3">
              <img src="/src/assets/images/icons/contacts/email.svg" alt="email">
              <span class="text-[#6C6C6C]">Email</span>
            </div>
            <div>
              <span class="font-bold">hello@cargopro.ru</span>
            </div>
          </div>
          <div class="flex flex-col gap-2">
            <div class="flex gap-3">
              <img src="/src/assets/images/icons/contacts/place.svg" alt="place">
              <span class="text-[#6C6C6C]">Адрес</span>
            </div>
            <div>
              <span class="font-bold">ТЦ АВИАПАРК, 1 ЭТАЖ</span>
            </div>
          </div>
        </div>
      </div>
      <div class="flex flex-col gap-14 pt-10">
        <div class="flex gap-2 items-center">
          <img src="/src/assets/images/icons/contacts/package.svg" alt="package">
          <h3 class="font-bold text-xl">Напишите нам</h3>
        </div>
        <form class="form flex flex-col gap-8">
          <input class="outline-none border-b border-gray-400" placeholder="Полное имя" type="text">
          <input class="outline-none border-b border-gray-400" placeholder="Номер телефона" type="text">
          <input class="outline-none border-b border-gray-400" placeholder="Email адрес" type="text">
          <textarea class="h-16 mb-4 outline-none resize-none border-b border-gray-400" placeholder="Сообщение" />
          <div>
            <Button button-classes="flex items-center gap-3">
              <img src="/src/assets/images/icons/subsidiary/send.svg" alt="">
              <span>Отправить</span>
            </Button>
          </div>
        </form>
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

.form {
  width: 420px;
}
</style>
