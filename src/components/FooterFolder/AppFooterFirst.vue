<script>
import { store } from "../../store.js";
export default {
  name: "AppFooterFirst",
  data() {
    return {
      store,
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer">
    <div
      class="container __container-inner d-flex justify-content-center gap-5 py-5 flex-wrap"
    >
      <div class="__banner text-white">
        <h2 class="fw-bold">Achieve Your Fitness Goals</h2>
        <p>
          Flexible membership packages to suit all levels of athlete and achieve
          your fitness goals
        </p>
      </div>
      <div class="__btn-ctnr py-4">
        <button type="button" class="btn btn-outline-light text-uppercase">
          Join us
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-image: url(/img/home-parallax.jpg);
  background-position: center;
}

p {
  text-align-last: center;
}
</style>
