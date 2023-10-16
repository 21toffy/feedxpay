<template>
  <div class="subnav shadow-sm">
    <div class="row">
      <div class="col-md-2">
        <ul class="list-unstyled subnav_sections">
          <li
            @click.prevent="showSection($event, 'currencies')"
            :class="type == 'currencies' ? 'text-primary' : 'text-dark'"
          >
            Currencies
          </li>
          <li
            @click.prevent="showSection($event, 'countries')"
            :class="type == 'countries' ? 'text-primary' : 'text-dark'"
          >
            Countries
          </li>
        </ul>
      </div>
      <div class="col-md-10">
        <div v-if="type == 'currencies'" class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>
                    <img src="~/assets/images/nigeria.svg" alt="" srcset="" />
                    Nigerian Naira
                  </li>
                  <li>
                    <img src="~/assets/images/ghana.svg" alt="" srcset="" />
                    Ghanian Cedis
                  </li>
                  <li>
                    <img src="~/assets/images/sa.svg" alt="" srcset="" /> South
                    African Rand
                  </li>
                  <li>
                    <img src="~/assets/images/kenya.svg" alt="" srcset="" />
                    Kenyan Shillings
                  </li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>
                    <img src="~/assets/images/us.svg" alt="" srcset="" /> US
                    Dollars
                  </li>
                  <li>
                    <img src="~/assets/images/canada.svg" alt="" srcset="" />
                    Canadian Dollars
                  </li>
                  <li>
                    <img src="~/assets/images/uk.svg" alt="" srcset="" />
                    British Pounds
                  </li>
                  <!-- <li><img src="~/assets/images/euro.svg" alt="" srcset=""> Euros</li> -->
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
                  <li>
                    <img src="~/assets/images/nigeria.svg" alt="" srcset="" />
                    Nigeria
                  </li>
                  <li>
                    <img src="~/assets/images/ghana.svg" alt="" srcset="" />
                    Ghana
                  </li>
                  <li>
                    <img src="~/assets/images/sa.svg" alt="" srcset="" /> South
                    Africa
                  </li>
                  <li>
                    <img src="~/assets/images/kenya.svg" alt="" srcset="" />
                    Kenya
                  </li>
                </ul>
              </div>
              <div class="col-md-4">
                <ul class="use_cases">
                  <li>
                    <img src="~/assets/images/us.svg" alt="" srcset="" /> United
                    States
                  </li>
                  <li>
                    <img src="~/assets/images/canada.svg" alt="" srcset="" />
                    Canada
                  </li>
                  <li>
                    <img src="~/assets/images/uk.svg" alt="" srcset="" />
                    United Kingdom
                  </li>
                  <!-- <li><img src="~/assets/images/euro.svg" alt="" srcset=""> Euros</li> -->
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
      type: "currencies",
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
