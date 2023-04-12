<script>
export default {
  name: "AppMainNews",
  data() {
    return {
      articles: [
        {
          id: 1,
          image: "blog1.jpg",
          title: "Train with free weights or your body weight?",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
        },
        {
          id: 2,
          image: "blog6.jpg",

          title: "Nutritional advice that will keep you training",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
        },
        {
          id: 3,
          image: "trainer4.jpg",

          title: "Simple principles for your next workout",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
        },
        {
          id: 4,
          image: "blog4.jpg",

          title: "To be number one, train like you're number two",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
        },
        {
          id: 5,
          image: "trainer3.jpg",

          title: "Top 5 mistakes every gym member make",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
        },
        {
          id: 6,
          image: "trainer1.jpg",

          title: "The myths of shredding body fat explored",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aspernatur, nostrum aut! Ipsum laboriosam voluptatum magnam illo earum quibusdam, at ea ab, sed quos nulla perferendis facere qui fugiat ratione! Atque.",
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
      <h2 class="text-uppercase text-white">Performance news</h2>
      <div class="__stars d-flex gap-2 py-4 mb-4">
        <i class="fa-regular fa-star"></i><i class="fa-regular fa-star"></i>
      </div>
      <div
        class="__cards-container d-flex flex-wrap justify-content-center align-items-start mb-5"
      >
        <div v-for="item in articles" class="__card">
          <div class="__img-ctnr">
            <img :src="`/img/${item.image}`" alt="" srcset="" />
          </div>
          <div class="__article-text p-4">
            <h6 class="text-white">{{ item.title }}</h6>
            <p class="__paragraph">{{ item.text }}</p>
          </div>
        </div>
      </div>
      <div class="__articles-button">
        <button
          type="button"
          class="btn btn-outline-secondary text-uppercase fw-bold"
        >
          Read all articles
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #25292b;
}

.__cards-container {
  gap: 30px;
}

.__cards-container .__card {
  width: calc(100% / 3 * 1 - (30px / 3 * 2));
  flex-basis: 350px;
  background-color: #1f2123;
}

.__img-ctnr {
  width: 100%;
}

.__card .__img-ctnr img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

/* .__article-text {
  
} */

.__paragraph {
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 4;
  color: #aaa9a9;
  /* white-space: nowrap; */
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 200px;
}

.__paragraph::after {
  content: "\2026";
}
</style>
