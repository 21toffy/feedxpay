<template>
  <div class="position-relative" ref="navigationMenu">
    <nav
      class="navbar navbar-expand-lg navbar-light bg-white border-bottom py-3"
    >
      <div>
        <a class="navbar-brand" href="/">
          <img
            src="~/assets/images/logo.svg"
            class="img-fluid"
            alt="feedxpay"
            srcset=""
          />
        </a>
      </div>
      <div class="collapse navbar-collapse" id="collapsibleNavId">
        <ul class="navbar-nav mr-auto mt-2 mt-lg-0 d-sm-none d-md-inline-flex">
          <li class="nav-item mx-3">
            <a class="nav-link" @click.prevent="showNav('solutions')" href="#"
              >Solutions</a
            >
          </li>
          <li class="nav-item mx-3">
            <a class="nav-link" @click.prevent="showNav('products')" href="#"
              >Products</a
            >
          </li>
          <li class="nav-item mx-3">
            <a class="nav-link" @click.prevent="showNav('company')" href="#"
              >Company</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link" @click.prevent="showNav('coverage')" href="#"
              >Coverage</a
            >
          </li>
        </ul>
        <button
          class="btn text-dark mr-4 my-2 my-sm-0 ml-auto ml-sm-auto ml-md-auto ml-lg-0 d-sm-none d-md-inline-flex"
          type="submit"
        >
          Sign In
        </button>
      </div>
      <div>
        <button class="btn btn-primary btn-sm my-2 my-sm-0" type="submit">
          Open an Account
        </button>
        <button
          class="navbar-toggler border-0"
          type="button"
          data-bs-toggle="modal"
          data-bs-target="#mobileSideNav"
          aria-controls="mobileSideNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </nav>
    <mobileNav></mobileNav>
    <SolutionsSubNavigation
      v-if="navIsShowing && active_nav == 'solutions'"
    ></SolutionsSubNavigation>

    <ProductsSubNavigation
      v-if="navIsShowing && active_nav == 'products'"
    ></ProductsSubNavigation>

    <CompanySubNavigation
      v-if="navIsShowing && active_nav == 'company'"
    ></CompanySubNavigation>

    <CoverageSubNavigation v-if="navIsShowing && active_nav == 'coverage'">
    </CoverageSubNavigation>
  </div>
</template>

<script>
import mobileNav from "./mobile-nav.vue";
import SolutionsSubNavigation from "./SolutionsSubNavigation.vue";
import ProductsSubNavigation from "./ProductsSubNavigation.vue";
import CompanySubNavigation from "./CompanySubNavigation.vue";
import CoverageSubNavigation from "./CoverageSubNavigation.vue";
export default {
  name: "Header",
  components: {
    mobileNav,
    SolutionsSubNavigation,
    ProductsSubNavigation,
    CompanySubNavigation,
    CoverageSubNavigation,
  },
  data() {
    return {
      active_nav: "",
      navIsShowing: false,
    };
  },
  methods: {
    showNav(type) {
      this.active_nav = type;
      if (!this.navIsShowing) {
        this.navIsShowing = true;
      } else if (this.navIsShowing) {
        this.active_nav = type;
      }
    },
    hideNav(event) {
      const navigationMenu = this.$refs.navigationMenu; // Change to the actual ref name
      if (!navigationMenu.contains(event.target)) {
        // Close the navigation menu or perform any desired action
        // You can use a data property to control the navigation menu's visibility
        this.navIsShowing = false;
      }
    },
  },
  mounted() {
    window.addEventListener("click", this.hideNav);
  },
  beforeDestroy() {
    // Remove the click event listener when the component is destroyed
    window.removeEventListener("click", this.hideNav);
  },
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
