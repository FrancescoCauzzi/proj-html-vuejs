<script>
import { store } from "./store.js";
import AppMain from "./components/MainFolder/AppMain.vue";
import AppHeader from "./components/HeaderFolder/AppHeader.vue";
import AppFooter from "./components/FooterFolder/AppFooter.vue";

export default {
  data() {
    return {
      store,
    };
  },
  components: {
    AppHeader,
    AppFooter,
    AppMain,
  },
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
</template>

<style scoped></style>
