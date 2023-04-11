<script>
export default {
  name: "AppMainFeatures",
  data() {
    return {
      items: [
        {
          id: 1,
          name: "strength",
          icon: "fa-solid fa-dumbbell",
          title: "Strength and Condition",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 2,
          name: "fitness",
          icon: "fa-solid fa-bicycle",
          title: "Fitness & Cardio",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 3,
          name: "flexibility",
          icon: "fa-solid fa-tornado",
          title: "Flexibility & Rest",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
        {
          id: 4,
          name: "health",
          icon: "fa-solid fa-heart-pulse",
          title: "Health & Diet",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Impedit,culpa autem deserunt in, nesciunt, obcaecati maxime ipsam voluptatibus.",
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner py-5 d-flex gap-3 flex-wrap justify-content-center"
    >
      <div
        v-for="item in items"
        class="__features d-flex flex-column gap-2 align-items-center"
        :class="`__${item.name}`"
      >
        <div class="__icon d-flex justify-content-center align-items-center">
          <i :class="`${item.icon}`"></i>
        </div>
        <h6 class="text-white">{{ item.title }}</h6>
        <div class="__star"><i class="fa-regular fa-star"></i></div>
        <p class="__paragraph">
          {{ item.description }}
        </p>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-image: url(../../../public/img/gym_bkgd_bw-compressor.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

.__features {
  flex-basis: 250px;
}
.__icon {
  color: #ee6059;
  font-size: 3em;
  border-radius: 50%;
  height: 110px;
  width: 110px;
  border: 2px solid #ee6059;
  /* padding: 10px 20px 10px 20px; */
}
.__star {
  color: gold;
}

.__paragraph {
  color: #aaa9a9;
  text-align: center;
}
</style>
