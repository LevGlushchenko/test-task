<template>
  <header class="header">
    <form action="#" class="header__search">
      <input type="text" name="search" placeholder="Поиск по системе" />
      <button type="submit">
        <svg-icon name="search"></svg-icon>
      </button>
    </form>

    <div class="header__user">
      <div class="user-photo">
        <img src="img/user-photo.jpg" alt="User photo" />
      </div>
      <div class="user-info">
        <strong>Alexander C.</strong>
        <span>Администратор</span>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss">
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__search {
    position: relative;
    flex: 0 0 100%;
    max-width: 50%;

    input {
      box-sizing: border-box;
      display: block;
      width: 100%;
      font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont,
        "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
      font-size: 16px;
      padding: 10px 15px;
      border-radius: 5px;
      border: 1px solid #cccccc;
      outline: 0;

      &::placeholder {
        color: #cccccc;
      }
    }

    button {
      position: absolute;
      top: 0;
      right: 0;
      border: 0;
      background-color: transparent;
      outline: 0;
      cursor: pointer;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 43px;
      width: 43px;

      svg {
        width: 1.5em;
        height: 1.5em;
        fill: #cccccc;
      }
    }
  }

  &__user {
    margin-left: auto;
    display: flex;
    align-items: center;

    .user-photo {
      margin-right: 10px;
      img {
        border-radius: 50%;
        width: 50px;
        height: 50px;
      }
    }

    .user-info {
      display: flex;
      flex-direction: column;
    }
  }
}
</style>
