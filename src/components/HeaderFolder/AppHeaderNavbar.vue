<script>
export default {
  name: "AppHeaderNavbar",
  data() {
    return {
      links: [
        { id: 1, name: "home" },
        { id: 2, name: "about us" },
        { id: 3, name: "facilities" },
        { id: 4, name: "membership" },
        { id: 5, name: "testimonials" },
        { id: 6, name: "blog" },
      ],
    };
  },
};
</script>
<template>
  <div class="text-white">
    <div class="container __nav-container d-flex justify-content-between">
      <div class="__logo">
        <img
          src="../../../public/img/gym_logo_1x.png"
          alt="Cannot retrieve image"
          srcset=""
        />
      </div>
      <div class="__links d-flex align-items-center">
        <ul class="d-flex gap-3 fw-bold">
          <li v-for="item in links">
            <a href="">{{ item.name.toUpperCase() }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<style scoped>
a {
  text-decoration: none;
  color: white;
}

a:hover {
  color: orange;
}

li {
  list-style-type: none;
}
</style>
