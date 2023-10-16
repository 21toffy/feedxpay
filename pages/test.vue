<template>
  <div class="subnav">
    <div class="row">
      <div class="col-2">
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
      <div class="col-10">
        <div v-if="type == 'industries'" class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-4">
                <ul class="use_cases">
                  <li>NGOs</li>
                  <li>Educational Institutions</li>
                  <li>Exporters</li>
                  <li>Importers</li>
                </ul>
              </div>
              <div class="col-4">
                <ul class="use_cases">
                  <li>Health & Pharmaceuticals</li>
                  <li>Telecommuncations</li>
                  <li>Travels</li>
                </ul>
              </div>
              <div class="col-4"></div>
            </div>
          </div>
        </div>
        <div v-else class="card bg-light w-100">
          <div class="card-body">
            <div class="row">
              <div class="col-4">
                <ul class="use_cases">
                  <li>Creator Economy</li>
                  <li>Global Payroll</li>
                  <li>Online Retail</li>
                </ul>
              </div>
              <div class="col-4">
                <ul class="use_cases">
                  <li>Manufacturing</li>
                  <li>Infastructure & Construction</li>
                </ul>
              </div>
              <div class="col-4"></div>
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
<style>
.subnav {
  padding: 50px;
  width: 100%;
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
  margin-top: 1.5rem !important;
}
</style>
