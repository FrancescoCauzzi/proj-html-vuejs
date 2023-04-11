<script>
import AppHeaderNavbar from "./AppHeaderNavbar.vue";
export default {
  name: "AppHeader",
  data() {
    return {};
  },
  components: {
    AppHeaderNavbar,
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-3">
    <AppHeaderNavbar></AppHeaderNavbar>
    <div class="__header-title d-flex flex-column align-items-center gap-3">
      <h1 class="text-uppercase __motivation-title fw-bold text-white">
        no pain no gain
      </h1>
      <h5 class="text-white">
        Motivation is what gets you started. Habit is what keeps you going.
      </h5>
      <button type="button" class="btn btn-outline-secondary">
        Join us today
      </button>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-image: url(/img/home-banner.jpg);
  background-size: cover;
  background-repeat: no-repeat;

  width: 100%;
}

.__motivation-title {
  font-size: 5em;
}
.__header-title {
  padding: 140px 0 140px 0;
  margin-bottom: 100px;
}
</style>
