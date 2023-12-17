<script setup>
import Button from "@/components/common/Button.vue";
</script>

<template>
  <footer class="bg-[#2B2B2B] w-full h-96 flex justify-center p-8 px-12">
    <div class="w-4/5 flex flex-col gap-14 justify-around">
      <div class="flex justify-between">
        <div class="flex flex-col gap-5">
          <div>
            <img class="mb-2" src="/src/assets/images/icons/logo-svgrepo.svg" alt="logo">
            <b class="text-[#F8F8F8]">CARGO PRO</b>
          </div>
          <div>
            <div class="mb-2">
              <h2 class="text-[#F8F8F8] font-bold">Подпишитесь на рассылку</h2>
              <p class="text-[#D7D7D7]">Мы будем отправлять вам полезную информаю раз в неделю</p>
            </div>
            <div class="flex gap-3">
              <input class="w-72 outline-none p-2 rounded-lg" placeholder="Ваш email" type="text"/>
              <Button>Отправить</Button>
            </div>
          </div>
        </div>
        <div class="flex justify-between text-[#AFAFAF] gap-16 items-center mr-20">
          <div class="flex flex-col gap-3 mt-3">
            <a class="hover:opacity-75" href="#"><b>Компания</b></a>
            <a class="hover:opacity-75" href="#">О нас</a>
            <a class="hover:opacity-75" href="#">Карьера</a>
            <a class="hover:opacity-75" href="#">Новости</a>
            <a class="hover:opacity-75" href="#">Контакты</a>
          </div>
          <div class="flex flex-col gap-3">
            <a class="hover:opacity-75" href="#"></a><b>Информация</b>
            <a class="hover:opacity-75" href="#">Правила</a>
            <a class="hover:opacity-75" href="#">Защита данных</a>
            <a class="hover:opacity-75" href="#">Cookies</a>
            <a class="hover:opacity-75" href="#">Настройки</a>
          </div>
          <div class="flex flex-col gap-3">
            <a class="text-white hover:opacity-75" href="#"></a><b>Ресурсы</b>
            <a class="hover:opacity-75" href="#">Блог</a>
            <a class="hover:opacity-75" href="#">Мероприятия</a>
            <a class="hover:opacity-75" href="#">Центр помощи</a>
            <a class="hover:opacity-75" href="#">Поддержка</a>
          </div>
        </div>
      </div>
      <div class="border-t border-gray-500 flex">
        <div class="flex justify-between px-5 text-center items-center mt-5 w-full">
          <div>
            <p class="text-[#D7D7D7]">© 2023 CARGO PRO. Все права защищены.</p>
          </div>
          <div class="flex gap-5">
            <img class="cursor-pointer hover:opacity-75" src="/src/assets/images/icons/contacts/twitter.svg"
                 alt="twitter">
            <img class="cursor-pointer hover:opacity-75" src="/src/assets/images/icons/contacts/link.svg" alt="link">
            <img class="cursor-pointer hover:opacity-75" src="/src/assets/images/icons/contacts/facebook.svg"
                 alt="facebook">
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
