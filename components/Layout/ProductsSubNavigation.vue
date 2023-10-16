<template>
  <div class="subnav shadow-sm">
    <div class="row">
      <div class="col-12 col-md-2">
        <ul class="list-unstyled subnav_sections">
          <li
            @click.prevent="showSection($event, 'business_use')"
            :class="type == 'business_use' ? 'text-primary' : 'text-dark'"
          >
            Business Use
          </li>
          <li
            @click.prevent="showSection($event, 'personal_use')"
            :class="type == 'personal_use' ? 'text-primary' : 'text-dark'"
          >
            Personal Use
          </li>
        </ul>
      </div>
      <div class="col-12 col-md-10">
        <div v-if="type == 'business_use'" class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-12 col-md-4">
                <ul class="use_cases">
                  <li><a href="/company/about-us"> Global Account </a></li>
                  <li><a href="/company/about-us"> Local Account </a></li>
                  <li><a href="/company/about-us"> Venture Debt </a></li>
                </ul>
              </div>
              <div class="col-12 col-md-4">
                <ul class="use_cases">
                  <li><a href="/company/about-us"> Invoice Financing </a></li>
                  <li><a href="/company/about-us"> Investment </a></li>
                  <li><a href="/company/about-us"> Start-Up </a></li>
                </ul>
              </div>
              <div class="col-4"></div>
            </div>
          </div>
        </div>
        <div v-else class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>
                    <a href="/company/about-us"> Wallet - Wallet Transfer </a>
                  </li>
                  <li>
                    <a href="/company/about-us"> Portfolio Management </a>
                  </li>
                  <li><a href="/company/about-us"> Cards </a></li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li><a href="/company/about-us"> Global Remittance </a></li>
                  <li><a href="/company/about-us"> Budgetting </a></li>
                  <li><a href="/company/about-us"> Mobile App </a></li>
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
      type: "business_use",
    };
  },
  methods: {
    showSection(e, type) {
      let ele = e;
      if (this.type !== type) {
        this.type = type;
      }
    },
  },
};
</script>
<style scoped>
a{
  text-decoration: none;
  color: #121212;
}
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
