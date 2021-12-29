<template>
  <nav class="nav container">
    <ul>
      <li>
        <a class="active" href="#">Главная</a>
      </li>
      <li>
        <a href="#">Про нас</a>
      </li>
      <li>
        <a href="#">Мебель под заказ</a>
      </li>
      <li>
        <a href="#">Шкафы купе</a>
      </li>
      <li>
        <a href="#">Доставка и оплата</a>
      </li>
      <li>
        <a href="#">Контакты</a>
      </li>
      <li>
        <a href="#">Письмо директору</a>
      </li>
      <li>
        <a href="#">Бренды</a>
      </li>
      <li>
        <a href="#">Дизайн интерьера</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
.nav {
  ul {
    list-style-type: none;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
  }

  a {
    text-decoration: none;
    display: inline-block;
    padding: 11px 19px;
    background: transparent;
    border-radius: 8px;
    font-size: 17px;
    line-height: 23.5px;
    font-weight: 600;
    transition: 0.2s ease-in-out;
  }

  .active {
    background-color: $backgroundColor;
  }

  a:hover {
    background-color: $backgroundColor;
  }
}
</style>