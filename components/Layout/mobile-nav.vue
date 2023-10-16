<template>
  <div>
    <div
      class="modal modal-right fade"
      id="mobileSideNav"
      tabindex="-1"
      role="dialog"
      aria-labelledby="modelTitleId"
      aria-hidden="true"
    >
      <div class="modal-dialog w-100" role="document">
        <div class="modal-content p-4">
          <div class="modal-header px-0 border-0 justify-content-end">
            <button
              type="button"
              class="btn btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            >
              <i class="bi bi-x-lg" style="font-size: x-large"></i>
            </button>
          </div>
          <div class="modal-body p-0">
            <div class="row h-100">
              <div class="col-12">
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-left border-bottom"
                    data-bs-toggle="collapse"
                    href="#solutions"
                    role="button"
                    aria-expanded="false"
                    aria-controls="solutions"
                  >
                    Solutions
                  </a>
                </p>
                <div class="collapse" id="solutions">
                  <SolutionsSubNavigation></SolutionsSubNavigation>
                </div>
                <!-- product -->
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-left border-bottom"
                    data-bs-toggle="collapse"
                    href="#product"
                    role="button"
                    aria-expanded="false"
                    aria-controls="product"
                  >
                    Product
                  </a>
                </p>
                <div class="collapse" id="product">
                  <ProductsSubNavigation></ProductsSubNavigation>
                </div>
                <!-- compnay -->
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-left border-bottom"
                    data-bs-toggle="collapse"
                    href="#company"
                    role="button"
                    aria-expanded="false"
                    aria-controls="company"
                  >
                    Company
                  </a>
                </p>
                <div class="collapse" id="company">
                  <CompanySubNavigation></CompanySubNavigation>
                </div>
                <!-- product -->
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-left border-bottom"
                    data-bs-toggle="collapse"
                    href="#coverage"
                    role="button"
                    aria-expanded="false"
                    aria-controls="coverage"
                  >
                    Coverage
                  </a>
                </p>
                <div class="collapse" id="coverage">
                  <CoverageSubNavigation></CoverageSubNavigation>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProductsSubNavigation from "./ProductsSubNavigation.vue";
import SolutionsSubNavigation from "./SolutionsSubNavigation.vue";
import CompanySubNavigation from "./CompanySubNavigation.vue";
import CoverageSubNavigation from "./CoverageSubNavigation.vue";

export default {
  name: "mobile-nav",
  methods: {
    close() {},
  },
  components: {
    ProductsSubNavigation,
    SolutionsSubNavigation,
    CompanySubNavigation,
    CoverageSubNavigation,
  },
};
</script>

<style></style>
