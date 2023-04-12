<script>
export default {
  name: "AppMainSignUp",
  data() {
    return {};
  },
};
</script>
<template>
  <div class="container-fluid __container-outer py-5" id="section4">
    <div
      class="container __container-inner d-flex gap-5 justify-content-center py-5 flex-wrap"
    >
      <div class="__image">
        <img
          src="/img/home_img-compressor.jpg"
          alt="Cannot retrieve image"
          srcset=""
        />
      </div>
      <div class="__form">
        <h4 class="text-white">Sign Up for a free training session</h4>
        <form action="">
          <div class="mb-3">
            <label for="textInput" class="form-label text-white">Name</label>
            <input
              type="text"
              class="form-control"
              id="textInput"
              aria-describedby="emailHelp"
            />
            <div id="emailHelp" class="form-text">
              We'll never share your email with anyone else.
            </div>
          </div>
          <div class="mb-3">
            <label for="emailInput" class="form-label text-white">Email</label>
            <input type="email" class="form-control" id="emailInput" />
          </div>

          <button type="submit" class="btn btn-danger w-100">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>
<style scoped="">
/* 1f2123 */
.__container-outer {
  background-color: #1f2123;
}

.__container-inner {
  min-width: 350px;
}
</style>
