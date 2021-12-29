<template>
  <div class="categories container">
    <Category v-for="cat in categories" :id="cat.id" :key="cat.id" />
  </div>
</template>

<script>
import Category from "./Category.vue";
export default {
  name: "Categories",
  components: { Category },
  data() {
    return {
      categories: [
        {
          id: 1,
          title: "Столы",
          text: "80шт",
          img: require("@/assets/categories/img1.png"),
        },
        {
          id: 2,
          title: "Кровати",
          text: "80шт",
          img: require("@/assets/categories/img2.png"),
        },
        {
          id: 3,
          title: "Тумбы",
          text: "80шт",
          img: require("@/assets/categories/img3.png"),
        },
        {
          id: 4,
          title: "Шкафы",
          text: "80шт",
          img: require("@/assets/categories/img4.png"),
        },
        {
          id: 5,
          title: "Стулья",
          text: "80шт",
          img: require("@/assets/categories/img5.png"),
        },
        {
          id: 6,
          title: "Диваны",
          text: "80шт",
          img: require("@/assets/categories/img6.png"),
        },
      ],
      cards: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/cards")
      .then((res) => res.json())
      .then((data) => (this.cards = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style lang="scss" scoped>
.categories {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(276px, 1fr));
  margin-top: 46px;
  column-gap: 44px;
  row-gap: 36px;
  margin-bottom: 50px;
}
</style>

