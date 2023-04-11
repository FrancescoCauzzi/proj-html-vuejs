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
  <div class="container-fluid __container-outer">
    <AppHeaderNavbar></AppHeaderNavbar>
  </div>
</template>
<style scoped>
.__container-outer {
  background-image: url(../../../public/img/home-banner.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  width: 100%;
}
</style>
