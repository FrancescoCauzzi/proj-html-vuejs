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
  <nav class="text-white navbar navbar-expand-lg navbar-light">
    <div class="container __nav-container d-flex justify-content-between">
      <div class="__logo mb-4">
        <img src="/img/gym_logo_1x.png" alt="Cannot retrieve image" srcset="" />
      </div>
      <!-- links che devono essere inseriti nel burger menu -->

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="collapse navbar-collapse text-white justify-content-end p-2"
        id="navbarSupportedContent"
      >
        <div class="__links d-flex align-items-center justify-content-center">
          <ul class="d-flex gap-3 fw-bold flex-wrap justify-content-center">
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
      <!--  -->
    </div>
  </nav>
</template>
<style scoped>
/* .__links {
  position: fixed;
  right: 20px;
} */

.navbar-toggler {
  color: white;
  background-color: #454d51;
  border-color: white;
}

.navbar-toggler-icon {
  color: white;
}

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
