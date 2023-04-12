<script>
import { store } from "../../store.js";
export default {
  name: "AppFooterSecond",
  data() {
    return {
      store,
      findUs: {
        address: "12345 North Main Street",
        city: "New York, NY 555555",
        phone: "1.800.555.6789",
        email: "info@your-domain.com",
      },
      recentPosts: [
        { id: 1, text: "Train with free weights or your body weight?" },
        { id: 2, text: "Nutritional advice that will keep you training" },
      ],
      openingTimes: [
        {
          id: 1,
          period: "weekdays",
          text: "Weekdays Monday - Friday",
          time: "09:00 - 19:00",
        },
        {
          id: 2,
          period: "weekend",
          text: "Weekends Saturday - Sunday",
          time: "09:00 - 21:00",
        },
      ],
    };
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5">
    <div
      class="container __container-inner d-flex flex-wrap justify-content-center py-5"
    >
      <div class="__find-us">
        <h6 class="text-uppercase mb-4">come find us</h6>
        <ul class="__description">
          <li>{{ findUs.address }}</li>
          <li>{{ findUs.city }}</li>
          <li>Phone: {{ findUs.phone }}</li>
          <li>Email: {{ findUs.email }}</li>
        </ul>
      </div>
      <div class="__recent-posts">
        <h6 class="text-uppercase mb-4">recent posts</h6>
        <ul>
          <li v-for="item in recentPosts">
            > {{ item.text }}
            <hr />
          </li>
        </ul>
      </div>
      <div class="__opening-times">
        <h6 class="text-uppercase mb-4">opening times</h6>
        <ul>
          <li v-for="item in openingTimes" class="mb-3">
            <span>{{ item.text }}</span>
            <br />
            <span class="__time">{{ item.time }}</span>
          </li>
        </ul>
      </div>
      <div class="__special-offer mb-4">
        <img src="/img/gym_ad-compressor.jpg" alt="" srcset="" />
      </div>
    </div>
  </div>
</template>
<style scoped>
.__container-outer {
  background-color: #1f2123;
}

.__container-inner > * {
  width: calc(100% / 4 * 1 - (30px / 4 * 3));
  flex-basis: 280px;
  margin-bottom: 60px;
  padding-right: 30px;
}

h6 {
  color: #6c777b;
}

ul {
  padding-left: 0;
}

li {
  color: #999999;
  list-style: none;
}

.__time {
  color: #4a5053;
}
</style>
