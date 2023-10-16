<template>
  <div class="position-relative" ref="navigationMenu">
    <nav
      class="navbar navbar-expand-lg navbar-light bg-primary py-3"
    >
      <div>
        <a class="navbar-brand" href="#">
          <img
            src="/inverted 1.png"
            class="img-fluid"
            alt="feedxpay"
            srcset=""
          />
        </a>
      </div>
      <button class="ml-auto btn text-white btn-sm my-2 my-sm-0" type="submit">
        Have an account? Sign in
      </button>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.navbar-brand img {
  height: 28px;
}

.subnav {
  z-index: 9999;
  position: absolute;
  background-color: white;
}

@media (max-width: 576px) {
  .navbar-brand {
    margin: 0;
  }
  .navbar-brand img {
    height: 20px;
  }
}
</style>
