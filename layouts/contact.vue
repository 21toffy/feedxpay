<template>
  <div class="content">
    <MiniHeader></MiniHeader>
    <div class="main">
      <nuxt />
    </div>
    <!-- <Footer></Footer> -->
  </div>
</template>

<script>
import MiniHeader from "@/components/Layout/MiniHeader.vue";
import Footer from "@/components/Layout/Footer.vue";
export default {
  name: "",
  components: { MiniHeader, Footer }
};
</script>
