<script>
export default {
  name: "AppMainFacilities",
  data() {
    return {
      images: [
        { id: 1, image: "home-image1.jpg" },
        { id: 2, image: "home-image2.jpg" },
        { id: 3, image: "home-image3.jpg" },
        { id: 4, image: "home-image4.jpg" },
        { id: 5, image: "home-image5.jpg" },
        { id: 6, image: "home-image6.jpg" },
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
      <h2 class="text-uppercase text-white">high performance facilities</h2>
      <div class="__stars d-flex gap-2 py-4">
        <i class="fa-regular fa-star"></i><i class="fa-regular fa-star"></i>
      </div>
      <div class="__images-container d-flex flex-wrap justify-content-center">
        <div v-for="item in images" class="__image-holder">
          <img :src="`/img/${item.image}`" alt="" srcset="" />
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #25292b;
}

.__images-container {
  gap: 40px;
}
.__image-holder {
  width: calc(100% / 3 * 1 - (40px / 3 * 2));
  flex-basis: 300px;
}

.__image-holder img {
  object-fit: cover;
  height: 100%;
  width: 100%;
}

.__stars {
  color: gold;
}
</style>
