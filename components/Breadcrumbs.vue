<template>
  <div class="breadcrumbs">
    <ul>
      <li>
        <a href="#">
          <svg-icon name="home" class="icon-home"></svg-icon>
        </a>
      </li>
      <li>
        <a href="#">
          Опросы
        </a>
      </li>
      <li>
        <span>Добавить опрос</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.breadcrumbs {
  padding: 20px 0;

  ul {
    display: flex;
    align-items: center;

    li {
      position: relative;
      padding-right: 15px;
      margin-right: 5px;

      &::before {
        content: "";
        position: absolute;
        top: 50%;
        right: 0;
        transform: translateY(-50%);
        width: 10px;
        height: 10px;
        background-image: url("../static/img/arrow.svg");
        background-repeat: no-repeat;
        background-size: cover;
      }

      &:last-child {
        padding-right: 0;

        &::before {
          display: none;
        }
      }
    }

    svg {
      transition: all 0.3s;
    }

    a {
      transition: all 0.3s;

      &:hover {
        color: #cccccc;

        svg {
          fill: #cccccc;
        }
      }
    }

    span {
      color: #cccccc;
    }

    svg.icon-home {
      width: 1.2em;
      height: 1.2em;
    }
  }
}
</style>
