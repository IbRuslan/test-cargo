<script>
import SuperButton from "@/components/common/Button.vue";

export default {
  components: {SuperButton},
  methods: {
    isRouteActive(routeName) {
      return this.$route.name === routeName;
    }
  }
};
</script>

<template>
  <header class="h-20 flex justify-center items-center">
    <div class="w-4/5">
      <div class="flex justify-between items-center px-10">
        <router-link
            :to="{ name: 'Home' }"
            :class="{ 'text-black': $route.name === 'Home', 'font-bold': $route.name === 'Home' }"
            class="text-[#6C6C6C]"
        >
          <img src="/src/assets/images/icons/logo-svgrepo.svg" alt="logo">
        </router-link>
        <nav class="text-lg flex justify-between gap-10">
          <router-link
              :to="{ name: 'Home' }"
              :class="{ 'text-black': $route.name === 'Home', 'font-bold': $route.name === 'Home' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Главная
          </router-link>
          <router-link
              :to="{ name: 'About' }"
              :class="{ 'text-black': $route.name === 'About', 'font-bold': $route.name === 'About' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            О компании
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Маркет
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Карго
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Информация
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Услуги
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Контакты
          </router-link>
          <router-link
              :to="{ name: '' }"
              class="text-[#6C6C6C] hover:text-black"
          >
            Блог
          </router-link>
        </nav>
        <SuperButton>Войти</SuperButton>
      </div>
    </div>
  </header>
</template>
