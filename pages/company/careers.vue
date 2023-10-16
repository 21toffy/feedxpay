<template>
  <div class="">
    <section class="section-1 position-relative mb-0 mb-lg-5 mb-md-5">
      <div class="row">
        <div class="col-12">
          <img
            src="~/assets/images/left.png"
            class="img-fluid d-block d-sm-block d-md-none d-lg-none d-xl-none mb-5 top"
            alt=""
            srcset=""
          />
        </div>
      </div>
      <img
        src="~/assets/images/left.png"
        class="left position-absolute d-none d-md-block d-lg-block"
        style="left: 30px"
        alt=""
      />
      <img
        src="~/assets/images/right.png"
        class="right position-absolute d-none d-md-block d-lg-block"
        style="right: 30px"
        alt=""
      />
      <div class="col-md-6 col-12 mx-auto">
        <h5 class="title-text h6 text-primary text-uppercase text-center mb-5">
          feedxpay careers
        </h5>
        <div class="text-center">
          <h3>Where dreamers and doers thrive</h3>
          <p class="text-left">
            We believe economic prosperity is possible. We also believe
            permission-less and successful entrepreneurship in emerging markets
            is possible.
          </p>
          <p class="text-left">
            Our mission is making economic prosperity accessible to everyone,
            and we are looking for the best and right people that can help us
            accomplish this.
          </p>
          <p class="text-left">
            We value unique contributions, embrace diversity in people and ideas
            and welcome everyone.
          </p>
        </div>
      </div>
      <div class="row">
        <div class="col-12">
          <img
            src="~/assets/images/right.png"
            class="img-fluid d-block d-sm-block d-md-none d-lg-none d-xl-none mb-5 bottom"
            alt=""
            srcset=""
          />
        </div>
      </div>
    </section>
    <section class="section-3">
      <div class="row">
        <div class="col-md-6 mx-auto text-center text-md-left text-lg-left">
          <h3>We help each other grow</h3>
          <p>
            We continuously seek truth, learn and improve in areas of making
            important decision that as to do with work, relationship, customer
            centricity and everything that is critical to our business.
          </p>

          <br />
          <div class="points">
            <template v-for="point in points">
              <div class="point mb-4">
                <div class="row align-items-center">
                  <div class="col-md-4 text-center">
                    <img
                      :src="point.img"
                      alt=""
                      style="height: 64px"
                      class="img-fluid"
                      srcset=""
                    />
                  </div>
                  <div class="col-md-8 text-center text-md-left text-lg-left">
                    <h6 class="font-weight-bold">{{ point.name }}</h6>
                    <p>{{ point.text }}</p>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>
    </section>
    <section class="section-4 bg-primary">
      <div class="py-3"></div>
      <div class="container">
        <img src="~/assets/images/theatre.png" class="img-fluid mb-5" alt="" />
        <div class="text-center">
          <h3 class="text-white">Feedxpay Experience</h3>
          <p class="text-white">
            Looking for a place to explore your knowledge? Come and join a team
            of problem solvers, artists, entrepreneurs, engineers and designers,
            customer service providers and creators in their best form, doing
            their best work in creating a new bank for transacting business and
            making payments easily and in quick time.
          </p>
        </div>
        <br />
        <br /><br /><br />
        <h2 class="text-white">Team Story</h2>
        <p class="text-white col-9 px-0">
          Get inspired with our team's story, how each person transitioned into
          the financial technology space.
        </p>
        <div class="row mt-5">
          <div class="col-md-4 col-6">
            <div class="card border-0 bg-transparent">
              <div class="img">
                <img
                  class="card-img-top"
                  src="/faruk.JPG"
                  alt="Card image cap"
                />
              </div>
              <div class="card-footer px-0">
                <h5 class="text-white">Rufai Faruk</h5>
                <small class="text-muted">CEO</small>
                <p class="text-success">
                  Read Story <i class="bi bi-arrow-top-right"></i>
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-4 col-6">
            <div class="card border-0 bg-transparent">
              <img
                class="card-img-top"
                src="/michael.png"
                alt="Card image cap"
              />
              <div class="card-footer px-0">
                <h5 class="text-white">Michael C. Ugwu</h5>
                <small class="text-muted">Product Manager</small>
                <p class="text-success">
                  Read Story <i class="bi bi-arrow-top-right"></i>
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-4 d-none">
            <div class="card border-0 bg-transparent">
              <img
                class="card-img-top"
                src="~/assets/images/team-3.png"
                alt="Card image cap"
              />
              <div class="card-footer px-0">
                <h5 class="text-white">Rufai Faruk</h5>
                <small class="text-muted">CEO</small>
                <p class="text-success">
                  Read Story <i class="bi bi-arrow-top-right"></i>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-5">
      <h5 class="text-center h3 mb-4">Our Benefits</h5>
      <div class="row">
        <div class="col-md-6 mb-4">
          <div class="row align-items-center">
            <div class="col-md-4 text-center">
              <img
                src="~/assets/images/money-bag.png"
                class="img-fluid mb-3"
                alt=""
                srcset=""
              />
            </div>
            <div class="col-md-8 text-center text-md-left text-lg-left">
              <h6 class="font-weight-bold mb-3">Competitive Salary</h6>
              <p>
                With FeedxPay, you'll enjoy super lowtransfer fees when sending
                money across borders. Say goodbye to those hidden charges! Keep
                more of your hard-earned money where it belongs, in your pocket.
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-6 mb-4">
          <div class="row align-items-center">
            <div class="col-md-4 text-center">
              <img
                src="~/assets/images/card-payment.png"
                class="img-fluid mb-3"
                alt=""
                srcset=""
              />
            </div>
            <div class="col-md-8 text-center text-md-left text-lg-left">
              <h6 class="font-weight-bold mb-3">Paid Leave</h6>
              <p>
                No more waiting for days to send money internationally.
                FeedxPay's advanced technology ensures your money gets to its
                destination in quick time. Quick, reliable, and hassle-free,
                that's the way to go!
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="row align-items-center">
            <div class="col-md-4 text-center">
              <img
                src="~/assets/images/section-5a.png"
                class="img-fluid mb-3"
                alt=""
                srcset=""
              />
            </div>
            <div class="col-md-8 text-center text-md-left text-lg-left">
              <h6 class="font-weight-bold mb-3">Allowances</h6>
              <p>
                No more waiting for days to send money internationally.
                FeedxPay's advanced technology ensures your money gets to its
                destination in quick time. Quick, reliable, and hassle-free,
                that's the way to go!
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="row align-items-center">
            <div class="col-md-4 text-center">
              <img
                src="~/assets/images/school.png"
                class="img-fluid mb-3"
                alt=""
                srcset=""
              />
            </div>
            <div class="col-md-8 text-center text-md-left text-lg-left">
              <h6 class="font-weight-bold mb-3">Learning and development</h6>
              <p>
                Rest assured, your money is safe with FeedxPay. Our cutting-edge
                security measures keep your funds and information protected at
                all times. Your financial security is our top priority.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section-5">
      <h5 class="text-center h3 mb-4">Open Roles</h5>
      <p class="text-center">No open roles available</p>
    </section>
  </div>
</template>

<script>
export default {
  name: "SectionFive",
  data() {
    return {
      points: [
        {
          img: require("~/assets/images/customer-support-call.png"),
          name: "Customer centricity",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/my-documents.png"),
          name: "Ownership",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/conversation.png"),
          name: "Clear communication",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/sports-medal.png"),
          name: "Obsession with high quality and excellence",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/transparency.png"),
          name: "Transparency",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/yoga.png"),
          name: "Adaptibility and flexibility",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/startup.png"),
          name: "Growth mindset",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
        {
          img: require("~/assets/images/innovation.png"),
          name: "Innovation",
          text: "We continuously seek  truth, learn and improve in areas of making important decision that as to do with work, relationship, customer centricity and everything that is critical to our business.",
        },
      ],
    };
  },
};
</script>

<style>
section {
  padding: 100px 60px 30px 60px;
}

.title-text {
  margin-bottom: 30px;
}

.section-1 img.left,
.section-1 img.right {
  max-height: 450px;
}

.section-1 img.top,
.section-1 img.bottom {
  height: 250px;
  /* position: absolute; */
  margin: 0;
}

.section-1 img.top {
  float: left;
}

.section-1 img.bottom {
  float: right;
}

.section-2 img,
.section-5 img {
  height: 64px;
}

.img {
  height: 293.4px;
  overflow: hidden;
}

.img img {
  object-position: center -120px;
  object-fit: cover;
}

section p {
  line-height: normal;
  color: #1d1d1f !important;
  font-size: 16px !important;
}

@media screen and (max-width: 576px) {
  section {
    padding: 30px 20px 30px 20px;
  }

  .img {
    height: auto;
    overflow: hidden;
  }

  .img img {
    object-position: center -20px;
    object-fit: cover;
  }

  section p {
    font-size: 13px !important;
    line-height: 20px !important;
  }
}

@media screen and (min-width: 577px) and (max-width: 768px) {
  section {
    padding: 80px 20px 30px 20px;
  }
  section p {
    font-size: 13px !important;
    line-height: 20px !important;
  }
}

@media screen and (min-width: 769px) and (max-width: 992px) {
  section {
    padding: 80px 20px 30px 20px;
  }
  section p {
    font-size: 13px !important;
    line-height: 20px !important;
  }
}
</style>
