<template>
  <div class="footer bg-light">
    <div class="quicklinks">
      <div class="row">
        <div class="col-md-3 mb-3">
          <nuxt-link to="/" class="navbar-brand p-0">
            <img
              src="~/assets/images/logo.svg"
              class="img-fluid mb-2"
              alt="feedxpay"
              srcset=""
            />
            <div class="d-flex justify-content-between">
              <a href=""><i class="text-muted bi-facebook"></i></a>
              <a href="https://www.linkedin.com/company/feedxpay/"
                ><i class="text-muted bi-linkedin"></i
              ></a>
              <a href="https://x.com/feedxpay?s=21&t=9UbgU9s2lOoKwSNXKIkytA"
                ><i class="text-muted bi-twitter"></i
              ></a>
              <a href="https://instagram.com/feedxpay?igshid=MzRlODBiNWFlZA=="
                ><i class="text-muted bi-instagram"></i
              ></a>
            </div>
          </nuxt-link>
        </div>
        <div class="col-md">
          <h6 class="text-primary">Company</h6>
          <ul class="sublinks">
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >About Us</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/blog"
                class="text-decoration-none text-dark"
                >Blog</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/careers"
                class="text-decoration-none text-dark"
                >Careers</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                class="text-decoration-none text-dark"
                to="/company/about-us"
                >Partners</nuxt-link
              >
            </li>
          </ul>
        </div>
        <div class="col-md">
          <h6 class="text-primary">Product</h6>
          <ul class="sublinks">
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Global Business Account</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Local Account</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Wallet-Wallet Treasury Management</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Start-Up</nuxt-link
              >
            </li>
            <li class="link-item d-none">Venture debt (coming soon)</li>
            <li class="link-item d-none">Invoice financing (coming soon)</li>
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Cards</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/company/about-us"
                class="text-decoration-none text-dark"
                >Mobile App</nuxt-link
              >
            </li>
          </ul>
        </div>
        <div class="col-md col-6">
          <h6 class="text-primary">Support</h6>
          <ul class="sublinks">
            <li class="link-item">
              <nuxt-link
                to="/help/contact"
                class="text-decoration-none text-dark"
                >Contact Sales</nuxt-link
              >
            </li>
            <li class="link-item">Community</li>
            <li class="link-item">
              <nuxt-link to="/help/faq" class="text-decoration-none text-dark"
                >FAQs</nuxt-link
              >
            </li>
            <li class="link-item">
              <nuxt-link
                to="/help/contact"
                class="text-decoration-none text-dark"
                >Become a Partner</nuxt-link
              >
            </li>
          </ul>
        </div>
        <div class="col-md col-6">
          <h6 class="text-primary">Legal</h6>
          <ul class="sublinks">
            <li class="link-item" style="cursor: pointer;" @click="$router.push('/legal/terms-of-use')">
              Terms of Use
            </li>
            <li class="link-item">Policy</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="row align-items-start align justify-content-between">
      <div class="col-md">
        <h5>Follow our latest news</h5>
        <form class="my-2 my-lg-0" @submit.prevent="saveEmails">
          <div class="row align-items-center">
            <div class="col-6">
              <input
                class="form-control mr-sm-2"
                type="emails"
                placeholder="Search"
                required
              />
            </div>
            <div class="col-6">
              <button class="btn my-2 my-sm-0 footer-btn" type="submit">
                <i class="text-primary bi-arrow-right"></i>
              </button>
            </div>
          </div>
        </form>
        <p class="font-weight-medium mt-2 small">
          Get information and updates on our financial services.
        </p>
      </div>
      <div class="col-md text-left text-md-right text-lg-right">
        <h6>Available on web and also on</h6>
        <div
          class="d-flex justify-content-start justify-content-md-end justify-content-lg-end"
        >
          <div class="d-flex store_images">
            <img src="/pngwing-1.png" class="img-fluid mr-3" alt="" />
            <img src="/pngwing-2.png" class="img-fluid" alt="" />
          </div>
        </div>
      </div>
    </div>
    <hr />
    <br />
    <p class="font-weight-bold small text-muted footer-last">
      Feedxpay is a product of Cyberpro Limited (RC: 1923872). Feedxpay and
      featured customers are financial technology companies and not a bank.
      Banking services are provided by our partnered banks who are duly licensed
      by CBN
    </p>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      email: "",
    };
  },
  methods: {
    saveEmails() {
      this.email = "";
    },
  },
};
</script>

<style>
.footer {
  padding: 50px 30px;
}
.navbar-brand img {
  height: 28px;
}

.navbar-brand i {
  font-size: 18px;
}

.quicklinks {
  padding-bottom: 60px;
}

.quicklinks h6 {
  font-size: 18px;
  padding-bottom: 25px;
  margin-bottom: 0;
}

.sublinks {
  list-style: none !important ;
  padding-left: 0;
}

.sublinks .link-item {
  font-size: 15px !important;
  font-weight: 500;
  padding-bottom: 25px;
}

.footer-btn {
  border-radius: 50%;
  outline: 1px solid #017a59;
}

.store_images img {
  height: 45px;
}
@media (max-width: 465px) {
  .navbar-brand {
    margin-bottom: 10px;
  }
  .navbar-brand img {
    height: 25px;
  }

  .navbar-brand i {
    font-size: 18px;
  }

  .quicklinks {
    padding-bottom: 60px;
  }

  .quicklinks h6 {
    font-size: 18px;
    padding-bottom: 15px;
    margin-bottom: 0;
  }

  .sublinks {
    list-style: none !important ;
    padding-left: 0;
  }

  .sublinks .link-item {
    font-size: 15px !important;
    font-weight: 500;
    padding-bottom: 15px;
  }

  .footer-btn {
    border-radius: 50%;
    outline: 1px solid #017a59;
  }

  .store_images img {
    height: 35px;
  }
  p.footer-last {
    font-size: 15px;
  }
}
</style>
