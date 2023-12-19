<script setup>
import Button from "@/components/common/Button.vue";
import ReviewCard from "@/components/modules/ReviewCard.vue";

const reviewItems = [
  {id: 1, title: 'Совершено перевозок', images: '/src/assets/images/icons/transportetion.svg', score: 950},
  {id: 2, title: 'Довольных клиентов', images: '/src/assets/images/icons/clients.svg', score: 1205},
  {id: 3, title: 'Членов команды', images: '/src/assets/images/icons/team.svg', score: 120},
]
</script>

<template>
  <div class="w-full flex justify-center py-32">
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
</template>

<style>
.review {
  width: 602px;
  height: 504px;
}
</style>