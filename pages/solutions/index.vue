<template>
  <div class="bg-light">
    <div class="container py-5">
      <div class="row">
        <div class="col-md-2">
          <div class="card card-body border-0">
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
        </div>
        <div class="col-md-10">
          <div v-if="type == 'use_cases'" class="card card-body border-0">
            <div class="section mb-4">
              <h5 class="text-primary">Creator Economy</h5>
              <h6>Fueling Creators and empowering Passion.</h6>
              <p>
                Our platform empowers content creators and creator platforms by
                providing seamless payment solutions through api integrations
                with creator platforms and a means for creators to receive fast
                payments. From receiving payments for digital content to
                managing subscription models and paying creatives, creators and
                creator platforms can focus on their businesses while we handle
                your financial transactions securely.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Global Payroll</h5>
              <h6>Seamless Paydays for your employees worldwide..</h6>
              <p>
                We simplify the complexities of global payroll management by
                helping to efficiently disburse salaries, manage tax deductions,
                and ensure compliance across different countries, streamlining
                the payroll process for businesses operating locally and
                internationally.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Online Retail</h5>
              <h6>Shop Smart, Pay Effortlessly.</h6>
              <p>
                Shop Smart, Pay Effortlessly. FeedXPay offers a robust platform
                to manage online transactions, secure payments and
                inter-currency trade.We also help to enhance your customer
                experience by providing various payment options while ensuring
                data security.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Manufacturing</h5>
              <h6>Building More Than Products, Crafting Trust.</h6>
              <p>
                Manufacturers encounter numerous challenges as they try to
                establish their global supply chain and reputation. We offer a
                reliable payment solution designed to facilitate your expansion
                and shield you from market uncertainties.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Infrastructure and Construction</h5>
              <h6>Constructing Excellence, with Precision payments.</h6>
              <p>
                Managing payments in the construction sector can be quite
                daunting and time-consuming but it becomes hassle-free with
                FeedXPay. Securely pay your contractors, suppliers, and
                subcontractors, ensuring that project timelines are met while
                maintaining financial transparency.
              </p>
            </div>
          </div>
          <div v-else class="card card-body border-0">
            <div class="section mb-4">
              <h5 class="text-primary">NGOs</h5>
              <h6>Changing Lives, One Payment at a Time.</h6>
              <p>
                Non-Governmental Organizations (NGOs) tirelessly strive to
                create a positive impact on the world and at FeedXPay, we offer
                more than just payment services to our clients. We deliver a
                specialized solution tailored for charities, facilitating
                cost-efficient payment sending and receiving. This ensures that
                a larger portion of funds reaches the areas that hold the utmost
                significance and that transparency is upheld.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Educational Institutions</h5>
              <h6>Education and tuition payments are simplified.</h6>
              <p>
                Going through the traditional exchange process for tuition
                payments can be quite tasking, but our platform offers
                educational institutions a platform for managing tuition
                payments, fees, and other financial transactions. Students and
                parents can make payments conveniently, ensuring a smoother
                administrative process.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Exporters and Importers</h5>
              <h6>
                Take your business across borders, buy and sell in all
                currencies.
              </h6>
              <p>
                Take your business across borders, buy and sell in all
                currencies. International trade transactions experience multiple
                constraints due to various policies. These constraints are
                simplified through FeedXPay's cross-border payment capabilities.
                Exporters and importers can securely send and receive payments,
                manage foreign exchange, and mitigate currency risks.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Health and Pharmaceuticals</h5>
              <h6>Healthier Payments to Create Brighterer Future.</h6>
              <p>
                Health is wealth, and the healthcare sector is one that is
                time-sensitive. Our speedy and reliable payment structure can
                save lives and avoid payment delays for treatments and supplies.
                The platform ensures that financial transactions within the
                industry are efficient and quick.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Telecommunications</h5>
              <h6>Stay connected wherever you go, we have got you covered.</h6>
              <p>
                Synchronize your telecommunications billing, prepaid services,
                and customer payments with Feedxpay and also pay for your bills
                on the feedxpay platforms. We provide a flexible platform to
                manage a variety of payment methods.
              </p>
            </div>
            <div class="section mb-4">
              <h5 class="text-primary">Traveling</h5>
              <h6>Exploring the World while Paying with Ease.</h6>
              <p>
                Skip the hassle of banks and agents and simplify payments for
                your travel. from booking flights and accommodations to managing
                travel expenses. We provide customers with a seamless payment
                experience during their journey
              </p>
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
body {
  background-color: #f8f9fa !important;
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
