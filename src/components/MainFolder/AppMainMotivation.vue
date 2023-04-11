<script>
export default {
  name: "AppMainMotivation",
  data() {
    return {
      images: [{ id: 1, name: "" }],
      text: " I fear not the man who has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times.",
      author: "Bruce Lee ° quote of the day",
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner d-flex flex-column align-items-center text-white"
    >
      <p class="w-50 text-center fs-5">"{{ text }}"</p>
      <div class="fw-bold">{{ author.toUpperCase() }}</div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-image: url(/img/home-testimonial-bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

.__container-inner {
  padding: 120px 0 120px 0;
}
</style>
