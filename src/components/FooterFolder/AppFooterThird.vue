<script>
import { store } from "../../store.js";
export default {
  name: "AppFooterThird",
  data() {
    return {
      store,
      social: [
        { name: "facebook", icon: "fa-brands fa-facebook-f" },
        { name: "twitter", icon: " fa-brands fa-twitter" },
        { name: "instagram", icon: " fa-brands fa-instagram" },
      ],
      credits: [
        { id: 1, text: "© Copyright 2012 - 2023 " },
        {
          id: 2,
          text: "Boolean Theme by Boolean Academy",
        },
        { id: 3, text: "All rights reserved" },
        { id: 4, text: "Powered by Boolean" },
      ],
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner d-flex justify-content-between px-5 flex-wrap"
    >
      <div
        class="__credits d-flex gap-2 align-items-center justify-content-center flex-wrap mb-3"
      >
        <span v-for="(item, index) in credits">
          {{ item.text }}
          {{ index < credits.length - 1 ? " | " : "" }}
        </span>
      </div>
      <div class="__social-media d-flex gap-3 justify-content-center">
        <div
          class="__social-media-item text-white d-flex justify-content-center align-items-center"
          v-for="item in social"
        >
          <a href="">
            <i :class="item.icon"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #1a1c1e;
}

.__credits {
  color: #999999;
}

.__social-media-item {
  background-color: #ee6059;
  height: 40px;
  width: 40px;
  cursor: pointer;
}

.__social-media a {
  color: white;
}
</style>
