<template>
  <aside class="sidebar">
    <div class="sidebar__logo">
      <a href="#"></a>
    </div>

    <nav class="sidebar__nav">
      <ul>
        <li>
          <a class="active" href="#">
            <svg-icon name="docs"></svg-icon>
            <span>Опросы</span>
          </a>
        </li>
        <li>
          <a href="#">
            <svg-icon name="users"></svg-icon>
            <span>Пользователи</span>
          </a>
        </li>
        <li>
          <a href="#">
            <svg-icon name="black-flag"></svg-icon>
            <span>Черные списки</span>
          </a>
        </li>
        <li>
          <a href="#">
            <svg-icon name="telephone"></svg-icon>
            <span>Колл-центр</span>
          </a>
        </li>
      </ul>
    </nav>

    <div class="sidebar__question">
      <a href="#">
        <span>?</span>
      </a>
    </div>
  </aside>
</template>

<script>
export default {};
</script>

<style lang="scss">
.sidebar {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 10px;
  border: 1px solid #ccc;
  height: 100vh;

  &__logo {
    width: 50px;
    height: 50px;
    margin-bottom: 100px;
    border-radius: 50%;
    background-color: red;
  }

  &__nav {
    li {
      margin-bottom: 5px;

      &:last-child {
        margin-bottom: 0;
      }
    }

    a {
      display: flex;
      flex-direction: column;
      align-items: center;
      color: #000000;
      border: 2px solid transparent;
      border-radius: 5px;
      transition: all 0.3s;
      padding: 10px 5px;
      text-align: center;

      &:hover {
        color: greenyellow;
        border-color: greenyellow;

        svg {
          fill: greenyellow;
        }
      }

      &.active {
        font-weight: 600;
        background-color: #cccccc;
        border-color: #cccccc;

        &:hover {
          font-weight: 600;
          background-color: #cccccc;
          border-color: #cccccc;
        }
      }
    }
  }

  &__question {
    margin-top: auto;

    a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 30px;
      height: 30px;
      color: green;
      font-size: 1.2em;
      border: 1px solid #000000;
      border-radius: 50%;
    }
  }
}
</style>
