<script>
import AppMainWC from "./AppMainWC.vue";
import AppMainSignUp from "./AppMainSignUp.vue";
import AppMainFeatures from "./AppMainFeatures.vue";
import AppMainTestimonials from "./AppMainTestimonials.vue";
import AppMainMotivation from "./AppMainMotivation.vue";
import AppMainTrainers from "./AppMainTrainers.vue";
import AppMainNews from "./AppMainNews.vue";

export default {
  name: "AppMain",
  data() {
    return {};
  },
  components: {
    AppMainWC,
    AppMainSignUp,
    AppMainFeatures,
    AppMainTestimonials,
    AppMainMotivation,
    AppMainTrainers,
    AppMainNews,
  },
};
</script>
<template>
  <AppMainWC></AppMainWC>
  <AppMainSignUp></AppMainSignUp>
</template>
<style scoped></style>
