<script>
export default {
  name: "AppMainTrainers",
  data() {
    return {
      trainers: [
        {
          id: 1,
          name: "Ann Baker",
          img: "trainer1.jpg",
          profession: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores delectus.",
          social: [
            { name: "facebook", icon: "fa-brands fa-facebook-f" },
            { name: "twitter", icon: " fa-brands fa-twitter" },
            { name: "instagram", icon: " fa-brands fa-instagram" },
          ],
        },
        {
          id: 2,
          img: "trainer3.jpg",
          name: "Anne Warren",
          profession: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores delectus.",
          social: [
            { name: "facebook", icon: "fa-brands fa-facebook-f" },
            { name: "twitter", icon: " fa-brands fa-twitter" },
            { name: "instagram", icon: " fa-brands fa-instagram" },
          ],
        },
        {
          id: 3,
          img: "trainer4.jpg",
          name: "Peter Rice",
          profession: "Personal Trainer",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Maiores delectus.",
          social: [
            { name: "facebook", icon: "fa-brands fa-facebook-f" },
            { name: "twitter", icon: " fa-brands fa-twitter" },
            { name: "instagram", icon: " fa-brands fa-instagram" },
          ],
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner d-flex flex-column align-items-center py-5"
    >
      <h2 class="text-uppercase text-white">Meet our trainers</h2>
      <div class="__stars d-flex gap-2 py-4 mb-4">
        <i class="fa-regular fa-star"></i><i class="fa-regular fa-star"></i>
      </div>
      <div class="__cards d-flex flex-wrap justify-content-center mb-5">
        <div v-for="item in trainers" class="__card">
          <div class="__img-container">
            <img :src="`/img/${item.img}`" alt="" srcset="" />
          </div>
          <div class="__description d-flex flex-column p-5 gap-3">
            <h6 class="text-white">{{ item.name }}</h6>
            <h6 class="text-white">{{ item.profession }}</h6>
            <p class="__paragraph">{{ item.text }}</p>
            <div class="__social-media d-flex gap-3">
              <div
                class="__social-media-item text-white d-flex justify-content-center align-items-center"
                v-for="subItem in item.social"
              >
                <a href="">
                  <i :class="subItem.icon"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="__articles-button">
        <button
          type="button"
          class="btn btn-outline-secondary text-uppercase fw-bold"
        >
          Meet our trainers
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #1f2123;
}

.__cards {
  gap: 40px;
}
.__card {
  width: calc(100% / 3 * 1 - (40px / 3 * 2));
  background-color: #25292b;
  flex-basis: 300px;
}
.__card img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.__paragraph {
  color: #aaa9a9;
}

.__social-media a {
  color: white;
}
.__social-media-item {
  background-color: #1f2123;
  height: 40px;
  width: 40px;
  cursor: pointer;
}
.__stars {
  color: gold;
}
</style>
