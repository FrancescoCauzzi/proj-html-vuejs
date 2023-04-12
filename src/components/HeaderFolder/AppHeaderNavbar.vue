<script>
export default {
  name: "AppHeaderNavbar",
  data() {
    return {
      active: 0,
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
  methods: {
    activateLink(index) {
      this.active = index;
    },
    scrollFunction(id) {
      let e = document.getElementById(id);
      e.scrollIntoView({
        block: "start",
        behavior: "smooth",
        inline: "start",
      });
    },
  },
};
</script>
<template>
  <div class="text-white">
    <div
      class="container __nav-container d-flex justify-content-between flex-wrap"
    >
      <div class="__logo mb-4">
        <img src="/img/gym_logo_1x.png" alt="Cannot retrieve image" srcset="" />
      </div>
      <div class="__links d-flex align-items-center justify-content-center">
        <ul class="d-flex gap-3 fw-bold flex-wrap justify-content-start">
          <li v-for="(item, index) in links">
            <a
              :class="this.active === index ? '__active' : ''"
              :href="`#section${item.id}`"
              @click="
                activateLink(index),
                  scrollFunction(`section${item.id}`) in links
              "
              >{{ item.name.toUpperCase() }}</a
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<style scoped>
/* .__links {
  position: fixed;
  right: 20px;
} */
a {
  text-decoration: none;
  color: white;
}

a:hover {
  color: grey;
}

.__active {
  color: orange;
}

li {
  list-style-type: none;
}

.__logo {
  min-width: 250px;
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}
</style>
