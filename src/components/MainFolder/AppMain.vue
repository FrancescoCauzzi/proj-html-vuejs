<script>
import AppMainWC from "./AppMainWC.vue";
import AppMainSignUp from "./AppMainSignUp.vue";
import AppMainFeatures from "./AppMainFeatures.vue";
import AppMainTestimonials from "./AppMainTestimonials.vue";
import AppMainFacilities from "./AppMainFacilities.vue";
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
    AppMainFacilities,
    AppMainMotivation,
    AppMainTrainers,
    AppMainNews,
  },
};
</script>
<template>
  <AppMainWC></AppMainWC>
  <AppMainSignUp></AppMainSignUp>
  <AppMainFeatures></AppMainFeatures>
  <AppMainTestimonials></AppMainTestimonials>
  <AppMainFacilities></AppMainFacilities>
  <AppMainMotivation></AppMainMotivation>
  <AppMainTrainers></AppMainTrainers>
</template>
<style scoped></style>
