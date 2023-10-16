<template>
  <div class="subnav shadow-sm">
    <div class="row">
      <div class="col-md-2">
        <ul class="list-unstyled subnav_sections">
          <li
            @click.prevent="showSection($event, 'use_cases')"
            :class="type == 'use_cases' ? 'text-primary' : 'text-dark'"
          >
            Use Cases
          </li>
          <li
            @click.prevent="showSection($event, 'industries')"
            :class="type == 'industries' ? 'text-primary' : 'text-dark'"
          >
            Industries
          </li>
        </ul>
      </div>
      <div class="col-md-10">
        <div v-if="type == 'industries'" class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-md-4">
                <ul class="use_cases">
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    NGOs
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Educational Institutions
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Exporters
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Importers
                  </li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Health & Pharmaceuticals
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Telecommuncations
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Travels
                  </li>
                </ul>
              </div>
              <div class="col-md-4"></div>
            </div>
          </div>
        </div>
        <div v-else class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-md-4">
                <ul class="use_cases">
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Creator Economy
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Global Payroll
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Online Retail
                  </li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Manufacturing
                  </li>
                  <li
                    style="cursor: pointer"
                    @click="$router.push('/solutions')"
                  >
                    Infastructure & Construction
                  </li>
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
      type: "use_cases",
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
