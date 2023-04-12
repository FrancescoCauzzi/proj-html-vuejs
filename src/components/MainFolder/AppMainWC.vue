<script>
export default {
  name: "AppMainWC",
  data() {
    return {};
  },
};
</script>
<template>
  <div class="container-fluid __container-outer text-center py-5" id="section2">
    <div
      class="container __container-inner d-flex align-items-center flex-column"
    >
      <h2 class="text-white">WORLD CLASS Fitness</h2>
      <div class="__stars d-flex gap-2 py-4">
        <i class="fa-regular fa-star"></i><i class="fa-regular fa-star"></i>
      </div>
      <p class="__paragraph w-50">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate
        autem assumenda quisquam repudiandae et ea! A nemo rerrum.
      </p>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #25292b;
}

.__stars {
  color: gold;
}

.__paragraph {
  color: #aaa9a9;
}
</style>
