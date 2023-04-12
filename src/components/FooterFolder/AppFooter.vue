<script>
import { store } from "../../store.js";
import AppFooterFirst from "./AppFooterFirst.vue";
import AppFooterSecond from "./AppFooterSecond.vue";
import AppFooterThird from "./AppFooterThird.vue";

export default {
  name: "AppFooter",
  data() {
    return {
      store,
    };
  },
  components: {
    AppFooterFirst,
    AppFooterSecond,
    AppFooterThird,
  },
};
</script>
<template>
  <AppFooterFirst></AppFooterFirst>
  <AppFooterSecond></AppFooterSecond>
  <AppFooterThird></AppFooterThird>
</template>
<style scoped></style>
