<script setup>

import Button from "@/components/common/Button.vue";
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
</template>