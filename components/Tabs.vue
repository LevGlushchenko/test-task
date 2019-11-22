<template>
  <div class="tabs">
    <ul>
      <li><a href="#">Параметры</a></li>
      <li><a href="#">Вопросы</a></li>
      <li><a href="#">Логика</a></li>
      <li><a href="#">Условия</a></li>
      <li><a class="active" href="#">Респонденты</a></li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.tabs {
  ul {
    display: flex;
    align-items: center;

    li {
      margin-right: 30px;

      &:last-child {
        margin-right: 0;
      }
    }

    a {
      display: block;
      color: green;
      padding: 10px 20px;
      border-bottom: 2px solid transparent;
      transition: all 0.3s;

      &.active,
      &:hover {
        color: #000000;
        border-color: greenyellow;
      }
    }
  }
}
</style>
