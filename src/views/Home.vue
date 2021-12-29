<template>
  <div class="home">
    <Header />
    <Banner />
    <Categories />
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
import Categories from "../components/Categories.vue";
import Header from "../components/Header.vue";

export default {
  components: { Header, Banner, Categories },
  name: "Home",
};
</script>
