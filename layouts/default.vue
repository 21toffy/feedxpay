<template>
  <div class="content">
    <Header></Header>
    <div class="main">
      <nuxt />
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "@/components/Layout/Header.vue";
import Footer from "@/components/Layout/Footer.vue";
export default {
  name: "",
  components: { Header, Footer }
};
</script>
