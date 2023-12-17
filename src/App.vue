<script>
import {defineComponent} from "vue";
import SuperHeader from "@/components/layout/Header.vue";
import SuperFooter from "@/components/layout/Footer.vue";

export default defineComponent({
  components: {SuperHeader, SuperFooter}
})
</script>

<template>
  <div id="app">
    <SuperHeader/>
    <router-view />
    <SuperFooter/>
  </div>
</template>

