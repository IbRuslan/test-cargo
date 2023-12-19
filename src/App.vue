<script>
import {defineComponent} from "vue";
import SuperHeader from "@/components/layout/Header.vue";
import SuperFooter from "@/components/layout/Footer.vue";

export default defineComponent({
  components: {SuperHeader, SuperFooter}
})
</script>

<template>
  <div class="app" id="app">
    <SuperHeader/>
    <main>
      <router-view />
    </main>
    <SuperFooter/>
  </div>
</template>



<style>
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex-grow: 1;
}
</style>