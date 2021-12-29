<template>
  <div class="home">
    <Header />
    <Banner />
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
import Header from "../components/Header.vue";

export default {
  components: { Header, Banner },
  name: "Home",
};
</script>
