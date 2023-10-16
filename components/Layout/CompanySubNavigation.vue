<template>
  <div class="subnav shadow-sm">
    <div class="row">
      <div class="col-md-2">
        <ul class="list-unstyled subnav_sections">
          <li class="text-primary">Company</li>
        </ul>
      </div>
      <div class="col-md-10">
        <div class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>
                    <a
                      href="/company/about-us"
                      class="text-decoration-none text-dark"
                      >About Us</a
                    >
                  </li>
                  <li>
                    <a
                      href="/company/careers"
                      class="text-decoration-none text-dark"
                      >Careers</a
                    >
                  </li>
                  <li>
                    <a
                      href="/company/blog"
                      class="text-decoration-none text-dark"
                      >Blogs</a
                    >
                  </li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>Partners</li>
                  <li>Customer Stories</li>
                </ul>
              </div>
              <div class="col-md-4"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {
      type: "company",
    };
  },
};
</script>
<style scoped>
.subnav {
  padding: 50px;
  width: 100%;
}
@media (max-width: 576px) {
  .subnav {
    padding: 10px;
    width: 100%;
  }
  .subnav_sections {
    display: flex;
    justify-content: space-between;
    font-weight: 500;
    cursor: pointer;
  }

  ul.use_cases {
    padding-left: 0;
  }

  .subnav_sections li {
    margin: 0px !important;
  }
}
ul.use_cases {
  list-style: none !important ;
}

ul.use_cases li {
  margin-bottom: 1.5rem !important;
}

.subnav_sections li {
  margin-bottom: 1.5rem !important;
  font-weight: 500;
  cursor: pointer;
}

.subnav_sections li:first-of-type {
  margin-top: 1.5rem;
}
</style>
