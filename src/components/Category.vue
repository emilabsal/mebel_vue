<template>
  <a href="#" class="card" v-if="card">
    <h4 class="title">{{ card.title }}</h4>
    <span class="text">{{ card.text }}</span>
    <img :src="card.img" alt="img" />
  </a>
</template>

<script>
export default {
  name: "Category",
  props: ["title", "text", "img", "id"],
  data() {
    return {
      card: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/cards/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.card = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style lang="scss" scoped>
.card {
  min-height: 236px;
  position: relative;
  z-index: 1;
  background-color: $backgroundColor;
  border-radius: 8px;
  padding: 20px 13px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  text-decoration: none;

  img {
    position: absolute;
    bottom: 0;
    right: 0;
  }

  .title {
    text-align: left;
    font-size: 24px;
    font-weight: 600;
    line-height: 32.68px;
    margin-bottom: 7px;
  }

  .text {
    font-size: 16px;
    line-height: 21.79px;
    color: #c4c4c4;
  }
}
</style>