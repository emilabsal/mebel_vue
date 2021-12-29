<template>
  <header class="header">
    <div class="top container">
      <img src="@/assets/header/delivery.svg" alt="deliver" />
      <p>Доставка и сборка по городу бесплатно!</p>
    </div>
    <div class="middle container">
      <p>mebel.ru - интернет-магазин качественной мебели</p>
      <div class="links">
        <a href="#">
          <img src="@/assets/header/geo.svg" alt="location" />
          Москва
        </a>
        <a href="#">
          <img src="@/assets/header/email.svg" alt="email" />
          mebel@yandex.ru
        </a>
      </div>
    </div>
    <div class="main container">
      <h1 class="logo">logo</h1>
      <button class="catalogue">
        <img src="@/assets/header/catalogue.svg" alt="catalogue" />
        Каталог
      </button>
      <form action="#" class="form">
        <input type="text" placeholder="Искать Товар" />
        <button>
          <img src="@/assets/header/search.svg" alt="search" />
        </button>
      </form>
      <a href="tel:+380937172929" class="phone">+38093-717-29-29</a>
      <div class="buttons">
        <button>
          <img src="@/assets/header/favor.svg" alt="favourite" />
        </button>
        <button>
          <img src="@/assets/header/cart.svg" alt="cart" />
        </button>
        <button>
          <img src="@/assets/header/avatar.svg" alt="avatar" />
        </button>
      </div>
    </div>
    <Navbar />
  </header>
</template>

<script>
import Navbar from "./Navbar.vue";
export default {
  components: { Navbar },
  name: "Header",
};
</script>

<style lang="scss" scoped>
.top {
  width: 100%;
  padding: 10px 0;
  background-color: $mainColor;
  display: flex;
  align-items: center;
  justify-content: center;
}

.top p {
  font-size: 16px;
  font-weight: 600;
  color: $lightColor;
  margin-left: 11px;
}

.middle {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 12px;
  padding-bottom: 10px;
  background: $backgroundColor;

  p {
    font-size: 13px;
    line-height: 17.7px;
  }
}

.links {
  display: flex;
  img {
    margin-right: 13px;
  }
  a {
    font-size: 13px;
    line-height: 17.7px;
    text-decoration: none;
    display: flex;
    align-items: center;

    &:first-child {
      margin-right: 75px;
    }
  }
}

.main {
  display: flex;
  align-items: center;
  padding-top: 35px;
  padding-bottom: 32px;
  justify-content: space-between;
}

.catalogue {
  border: none;
  outline: none;
  padding: 18px 35px;
  background-color: $mainColor;
  border-radius: 8px;
  font-weight: 600;
  color: $lightColor;
  display: flex;
  align-items: center;
  cursor: pointer;
  margin-left: 87px;

  img {
    margin-right: 6px;
  }
}

.form {
  display: flex;
  border-radius: 8px;
  overflow: hidden;
  height: 58px;
  flex-grow: 1;
  margin-left: 75px;
  margin-right: 102px;
  input {
    height: 100%;
    background: $backgroundColor;
    padding: 5px 24px;
    border: none;
    outline: none;
    display: flex;
    align-items: center;
    flex-grow: 1;

    &::placeholder {
      font-size: 15px;
      color: $placeholder;
    }
  }

  button {
    background-color: $backgroundColor;
    outline: none;
    border: none;
    padding: 0 30px;
    cursor: pointer;
  }
}

.phone {
  font-size: 20px;
  line-height: 27.24px;
  font-weight: 600;
  text-decoration: none;
}

.buttons {
  button {
    outline: none;
    border: none;
    background: transparent;
    margin-left: 70px;
    cursor: pointer;
  }
}
</style>