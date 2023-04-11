<script>
export default {
  name: "AppMainTestimonials",
  data() {
    return {
      testimonials: [
        {
          id: 1,
          name: "Tara Smith",
          img: "review_1-compressor.jpg",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 2,
          name: "Simon Chel",
          img: "review_3-compressor-2.jpg",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 3,
          name: "Jen Wirth",
          img: "review_2-compressor.jpg",

          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 4,
          name: "Jeff Glum",
          img: "review_4-compressor-2.jpg",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner py-5 d-flex flex-column align-items-center"
    >
      <h2 class="text-uppercase text-white">Real world results</h2>
      <div class="__stars d-flex gap-2 py-4">
        <i class="fa-regular fa-star"></i><i class="fa-regular fa-star"></i>
      </div>
      <div class="__card-container d-flex flex-wrap">
        <div v-for="item in testimonials" class="__card d-flex p-5">
          <div class="__img">
            <img
              :src="`../../../public/img/${item.img}`"
              alt="Cannot retrieve image"
              srcset=""
            />
          </div>
          <div class="__card-paragraph px-3">
            <p>"{{ item.text }}""</p>
            <div class="__name fw-bold">- {{ item.name }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #25292b;
}

.__card {
  width: calc(100% / 2 * 1 - (30px / 2 * 1));
  background-color: #1f2123;
}

.__card-paragraph {
  font-style: italic;
}
.__card-container {
  gap: 30px;
  color: #aaa9a9;
}
.__stars {
  color: gold;
}
</style>
