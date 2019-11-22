<template>
  <div class="condition-block">
    <div class="left-col">
      <div class="condition-block__title">Условие {{ index + 1 }}</div>
    </div>

    <div class="right-col">
      <select class="condition-block__select" name="condition">
        <option selected disabled>Выберите условие</option>
        <option value="respondent-age">Возраст респондента</option>
        <option value="loyalty-card-type">Тип карты лояльности</option>
        <option value="loyalty-card-status">Статус карты лояльности</option>
      </select>

      <a
        class="condition-block__delete"
        href="#"
        @click.prevent="removeCondition()"
      >
        <svg-icon name="delete"></svg-icon>
        <span>Удалить условие</span>
      </a>
    </div>

    <div class="condition-block__separator">И</div>
  </div>
</template>

<script>
export default {
  props: ["index", "array"],

  data() {
    return {
      types: []
    };
  },

  methods: {
    removeCondition() {
      this.array.splice(this.index, 1);
    }
  }
};
</script>

<style lang="scss">
.condition-block {
  position: relative;
  display: flex;
  justify-content: space-between;
  padding: 10px 20px 100px 20px;

  .left-col {
    flex: 0 0 100%;
    max-width: calc(30% - 10px);
  }

  .right-col {
    flex: 0 0 100%;
    max-width: calc(70% - 10px);
  }

  &__title {
    font-weight: 600;
    font-size: 14px;
  }

  &__select {
    display: block;
    width: 100%;
    padding: 10px 5px;
    border: 1px solid #cccccc;
    border-radius: 5px;
    outline: 0;
  }

  &__separator {
    position: absolute;
    bottom: -10px;
    left: 20px;
    z-index: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 30px;
    height: 30px;
    border-radius: 5px;
    background-color: #cccccc;
  }

  &__delete {
    position: absolute;
    bottom: 20px;
    right: 20px;
    display: flex;
    align-items: center;
    padding: 10px 5px;
    background-color: #ffffff;
    color: red;
    border-radius: 5px;
    box-shadow: 1px 1px 5px rgba(red, 0.5);

    svg {
      width: 1.2em;
      height: 1.2em;
      fill: red;
      margin-right: 5px;
    }
  }

  &:nth-of-type(1n) {
    background-color: coral;

    .condition-block__title {
      color: darken(coral, 20%);
    }

    .condition-block__separator {
      background-color: darken(coral, 20%);
    }
  }
  &:nth-of-type(2n) {
    background-color: #bcbcff;

    .condition-block__title {
      color: darken(#bcbcff, 20%);
    }

    .condition-block__separator {
      background-color: darken(#bcbcff, 20%);
    }
  }
  &:nth-of-type(3n) {
    background-color: green;

    .condition-block__title {
      color: darken(green, 20%);
    }

    .condition-block__separator {
      background-color: darken(green, 20%);
    }
  }
  &:nth-of-type(4n) {
    background-color: grey;

    .condition-block__title {
      color: darken(grey, 20%);
    }

    .condition-block__separator {
      background-color: darken(grey, 20%);
    }
  }
}
</style>
