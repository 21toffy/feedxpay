<template>
  <div>
    <section class="section-1">
      <div class="row align-items-center">
        <div class="col-md-6 order-1 order-md-0 order-lg-0">
          <h1>
            The <span class="text-primary">NeoBank</span> for <br />
            transcending borders. <br />
            Built for global spending and multinational operations
          </h1>
          <p>
            Make all your payments across borders effortlessly under one roof.
            It is quick, easy, safe and efficient.
          </p>
          <button type="submit" class="btn btn-primary mt-4">
            Get Started Now
          </button>
        </div>
        <div
          class="col-md-6 order-0 order-md-1 order-lg-1 mb-4 mb-md-0 mb-lg-0"
        >
          <div class="video-container">
            <video
              ref="video"
              class="position-absolute"
              autoplay
              loop
              muted
              crossorigin="anonymous"
              playsinline
              preload="auto"
              @loadeddata="handleVideoLoaded"
            >
              <source src="/video/video.mp4" type="video/mp4" />
            </video>
            <div v-if="isLoading" class="loading-overlay">
              <img src="~/assets/images/logo.svg" alt="Loading Icon" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-2 scroll-container">
      <h2 class="h3 text-center font-weight-bold">Some of our Partners</h2>
      <hr style="width: 150px; color: #223d30" />
      <div class="scroll-container">
        <div class="scrollable_images" style="margin-bottom: 35px">
          <img
            v-for="image in partners"
            :src="image.img"
            style="margin-right: 100px"
            alt=""
            srcset=""
          />
        </div>
      </div>
    </section>
    <section class="section-3 bg-light">
      <h2 class="h3 text-center font-weight-bold">
        All your financial modules on one platform
      </h2>
      <hr style="width: 150px; color: #223d30" />
      <p class="text-center">
        Built to make business transactions easier, helping you sort payments
        seamlessly in quick time.
      </p>
      <br />
      <div class="container-fluid">
        <div class="row row-cols-md-2 mb-4 row-1">
          <div class="col-sm-6 col-md-6 col-lg-7 mb-3 mb-md-0 mb-lg-0">
            <div class="card h-100">
              <div class="card-body">
                <img
                  src="~/assets/images/section-3l.svg"
                  class="img-fluid w-100 d-none d-md-block d-lg-block"
                  alt=""
                />
                <img
                  src="~/assets/images/section-3l-sm.png"
                  class="img-fluid w-100 d-block d-md-none d-lg-none"
                  alt=""
                />
              </div>
              <div class="card-footer bg-transparent border-0">
                <h6 class="text-primary mb-3">PAYMENTS</h6>
                <h4>Multi currency virtual account</h4>
                <p>
                  The all-in-one account you can open in 10minutes. Unlimited
                  transaction history invoicing
                </p>
              </div>
            </div>
          </div>
          <div class="col-sm-6 col-md-6 col-lg-5 col-sm-6">
            <div class="card h-100 mb-4 bg-primary">
              <div class="card-body">
                <div class="card mb-5">
                  <div class="p-4">
                    <div
                      class="d-flex scrollable_cards overflow-auto"
                      style="white-space: nowrap"
                    >
                      <div class="card currency_cards bg-primary">
                        <div class="card-body text-white">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/us.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">2,000.00</h6>
                          <p class="small mb-0">US Dollar</p>
                        </div>
                      </div>
                      <div class="card border currency_cards">
                        <div class="card-body">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/spain.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">1,500.00</h6>
                          <p class="small mb-0">Spanish Euro</p>
                        </div>
                      </div>
                      <div class="card border currency_cards">
                        <div class="card-body">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/canada.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">3,500.00</h6>
                          <p class="small mb-0">Canadian Dollar</p>
                        </div>
                      </div>
                      <div class="card border currency_cards">
                        <div class="card-body">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/uk.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">20,000.00</h6>
                          <p class="small mb-0">British Pounds</p>
                        </div>
                      </div>
                      <div class="card border currency_cards">
                        <div class="card-body">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/sa.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">5,000.00</h6>
                          <p class="small mb-0">SA Rand</p>
                        </div>
                      </div>
                      <div class="card border currency_cards">
                        <div class="card-body">
                          <div
                            class="d-flex justify-content-between align-items-start"
                          >
                            <img
                              src="~/assets/images/france.svg"
                              class="img-fluid mb-3"
                              alt=""
                              srcset=""
                            />
                            <i class="bi-arrow-up-right"></i>
                          </div>
                          <h6 class="mb-1">10,000.00</h6>
                          <p class="small mb-0">France Euro</p>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="card-footer bg-transparent border-0 pb-3">
                    <h6 class="text-primary mb-1 mb-md-3 mb-lg-3">
                      SWIFT PAYMENTS
                    </h6>
                    <h4 class="">Wire money in 20+ currencies.</h4>
                  </div>
                </div>
                <p class="text-white">
                  Send and receive money from any
                  <br class="d-none d-md-block d-lg-block" />
                  country in quick time.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="row row-cols-md-2 row-2">
          <div class="col-sm-6 col-md-6 col-lg-5">
            <div class="card h-100 bg-primary">
              <div class="card-body">
                <div class="card">
                  <div class="p-3">
                    <div class="d-flex pt-3 justify-content-between">
                      <p class="text-dark">Our physical and virtual card</p>
                      <span class="d-sm-none d-md-none d-lg-block d-none"
                        >Learn more</span
                      >
                    </div>
                    <div
                      class="d-flex scrollable_cards overflow-auto"
                      style="white-space: nowrap; margin-bottom: 25px"
                    >
                      <div class="card w-100">
                        <img
                          src="~/assets/images/card-1.svg"
                          alt=""
                          srcset=""
                        />
                      </div>
                      <div class="card w-100">
                        <img
                          src="~/assets/images/card-1.svg"
                          alt=""
                          srcset=""
                        />
                      </div>
                      <div class="card w-100">
                        <img
                          src="~/assets/images/card-1.svg"
                          alt=""
                          srcset=""
                        />
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="card-footer text-white mb-3 bg-transparent border-0">
                <h6 class="text-white mb-3">ACCOUNT HOLDER</h6>
                <h4>Both payment cards are fast.</h4>
                <p class="text-white">
                  There is no restrictions to our cards. You can use either or
                  both for payments.
                </p>
              </div>
            </div>
          </div>
          <div class="col-sm-6 col-md-6 col-lg-7">
            <div class="card h-100 mb-4">
              <div class="card-body">
                <img
                  src="~/assets/images/section-3r.svg"
                  class="img-fluid w-100 d-none d-md-block d-lg-block"
                  alt=""
                />
                <img
                  src="~/assets/images/section-3r-sm.png"
                  class="img-fluid w-100 d-block d-md-none d-lg-none"
                  alt=""
                />
              </div>
              <div class="card-footer bg-transparent border-0">
                <h6 class="text-primary mb-3">ANALYTICS & REPORTS</h6>
                <h4>Transaction analytics & reports</h4>
                <p>Get access to AI powered tools for transaction analysis</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-4">
      <h2 class="h3 text-center font-weight-bold">
        Customized cards available for every payments
      </h2>
      <hr style="width: 150px; color: #223d30" />
      <div class="row gx-3 h-100">
        <div class="col-md-6 col-lg-6 my-auto">
          <h3 class="font-weight-bold">
            One tool, one easy way to transact business effortlessly.
          </h3>
          <div class="col-md-10 px-0">
            <p class="">
              Our solution makes it easy for businesses, companies and other
              financial institutions to make global payment and receive with
              multiple currencies.
            </p>
            <nuxt-link
              to="/help/contact"
              type="button"
              id="form1Submit"
              aria-label=""
              class="btn btn-primary"
            >
              Contact Sales
            </nuxt-link>
          </div>
        </div>
        <div class="col-md-6 mt-md-0 mt-lg-0 mt-5">
          <img src="~/assets/images/section-1a.png" alt="" class="img-fluid" />
        </div>
      </div>
    </section>
    <div class="footerline text-center">
      <h3 class="font-weight-bold mb-3">
        Sign up in minutes. Join the movement.
      </h3>
      <p class="col-md-10 col-sm-11 col-12 mx-auto text-white line mb-3">
        Our goal is to protect what's most precious to entrepreneurs: their
        time, energy and focus. We offer the best financial services for you, in
        terms of our services are secure and easy to use.
      </p>
      <button class="btn btn-outline-light" style="border-radius: 15px">
        Get Started
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      isLoading: true,
      partners: [
        {
          img: require("~/assets/images/providusbank.png"),
        },
        {
          img: require("~/assets/images/maplerad.png"),
        },
        {
          img: require("~/assets/images/wema.png"),
        },
        {
          img: require("~/assets/images/fincra-1.png"),
        },
        {
          img: require("~/assets/images/gtb.png"),
        },
        {
          img: require("~/assets/images/anchor.jpeg"),
        },
      ],
    };
  },
  methods: {
    async handleVideoLoaded() {
      this.isLoading = false;
      const video = this.$refs.video;
      if (video) {
        await video.play(); // Start playing the video
      }
    },
  },
};
</script>

<style>
section {
  padding: 100px 60px 30px 60px;
}

.footerline {
  padding: 75px;
  background-color: #223d30;
  color: #fff;
}

.video-container {
  position: relative;
  height: 500px;
  width: 100%;
  overflow-y: hidden;
}

.video-container video {
  height: 640px;
  right: 0;
  top: -15%;
  /* bottom: 0; */
}

.loading-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.8);
  z-index: 9999;
}

.loading-overlay img {
  width: 100px; /* adjust as needed */
  height: auto;
}

.horizontal-scroll {
  display: flex;
  overflow-x: auto; /* Enable horizontal scrolling */
  white-space: nowrap; /* Prevent wrapping */
}

.section-3 {
  background-color: #f5f5f7;
}

.section-3 .card {
  border-radius: 20px;
  border: 0;
}

.scrollable_cards::-webkit-scrollbar,
.scrollable_images::-webkit-scrollbar {
  display: none;
}

.scroll-container {
  width: 100%; /* Adjust to your desired width */
  overflow: hidden;
}

.scrollable_images {
  display: flex;
  animation: scroll 40s linear infinite; /* Adjust the animation duration as needed */
}

@keyframes scroll {
  0% {
    transform: translateX(100%); /* Move images out on the right */
  }
  100% {
    transform: translateX(-100%); /* Move images in from the left */
  }
}

/* Hide scrollbar for IE, Edge and Firefox */
.scrollable_cards,
.scrollable_images {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

.scrollable_images img {
  min-height: 50px;
  max-height: 75px;
  margin-right: 10px;
}

.row-1 .currency_cards {
  min-width: 150px;
  border-radius: 12px;
  margin-right: 10px;
}

.row-2 .scrollable_cards .card {
  min-width: 310px;
  border-radius: 15px;
  margin-right: 10px;
}

.row-2 .scrollable_cards .card img {
  width: 310px;
}

@media screen and (max-width: 465px) {
  section {
    padding: 80px 20px;
  }

  section.section-1 {
    padding-top: 50px;
    padding-bottom: 100px;
  }

  .video-container {
    position: relative;
    height: 300px;
    width: 100%;
    overflow: hidden;
  }

  .video-container video {
    /* height: 200px; */
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    /* min-height: 100%; */
    width: auto;
    height: 350px;
  }
  .footerline {
    padding: 25px;
    background-color: #223d30;
    color: #fff;
  }

  .footerline p {
    font-size: 14px !important;
    line-height: normal;
  }

  .section-2 .row.overflow-auto {
    flex-wrap: nowrap;
  }

  .scrollable_images img {
    min-height: 20px;
    max-height: 40px;
    margin-right: 15px;
  }
}

@media (max-width: 768px) {
  section {
    padding: 80px 30px;
  }

  section.section-1 {
    padding-top: 100px;
    /* padding-bottom: 80px; */
  }

  .video-container {
    position: relative;
    height: 300px;
    width: 100%;
    /* object-fit: contain; */
  }

  .video-container video {
    /* height: 200px; */
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    /* min-height: 100%; */
    width: auto;
    height: 400px;
  }

  .row-1 .currency_cards {
    width: 130px;
  }

  .row-2 .scrollable_cards .card {
    min-width: 180px;
  }

  .row-2 .scrollable_cards .card img {
    width: 180px;
  }
}

@media (min-width: 769px) and (max-width: 991px) {
  .row-2 .scrollable_cards .card {
    min-width: 200px;
  }

  .row-2 .scrollable_cards .card img {
    width: 200px;
  }

  .video-container {
    position: relative;
    height: 300px;
    width: 100%;
    /* object-fit: contain; */
  }

  .video-container video {
    /* height: 200px; */
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    /* min-height: 100%; */
    width: auto;
    height: 400px;
  }
}
</style>
