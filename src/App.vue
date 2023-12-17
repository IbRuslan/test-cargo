<script>
import {defineComponent} from "vue";
import SuperHeader from "@/components/layout/Header.vue";
import SuperFooter from "@/components/layout/Footer.vue";
import NotFound from "@/views/NotFound.vue";

export default defineComponent({
  components: {NotFound, SuperHeader, SuperFooter}
})
</script>

<template>
  <div id="app">
    <SuperHeader/>
    <router-view />
    <SuperFooter/>
  </div>
</template>

