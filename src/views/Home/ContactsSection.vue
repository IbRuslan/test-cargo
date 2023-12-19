<script setup>
import Button from "@/components/common/Button.vue";
</script>

<template>
  <div class="w-full flex justify-center py-40">
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
.form {
  width: 420px;
}
</style>