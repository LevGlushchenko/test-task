<template>
  <form class="survey-form">
    <legend class="survey-form__title">Добавить опрос</legend>

    <template v-for="(condition, index) in conditions">
      <ConditionBlock :index="index" :array="conditions" :key="index" />
    </template>

    <div class="survey-form__add" @click="addCondition()">
      <div>
        <i class="icon-plus">+</i>
        <p>
          Нажмите, чтобы добавить новое условие выборки. <br />
          Все условия связываються между собой логической "И"
        </p>
      </div>
    </div>

    <div class="survey-form__buttons">
      <a href="#">
        <span>Протестировать опрос</span>
      </a>
      <a href="#">
        <span>Далее</span>
        <svg-icon name="arrow"></svg-icon>
      </a>
    </div>
  </form>
</template>

<script>
import ConditionBlock from "@/components/ConditionBlock";

export default {
  data() {
    return {
      conditions: []
    };
  },

  components: {
    ConditionBlock
  },

  methods: {
    addCondition() {
      this.conditions.push({});
    }
  }
};
</script>

<style lang="scss">
.survey-form {
  display: block;
  width: 100%;
  border-top: 1px solid greenyellow;
  box-shadow: 2px 2px 5px rgba(#000, 0.3);
  background-color: #cccccc;

  &__title {
    padding: 20px;
    padding-bottom: 5px;
    color: #cccccc;
    font-weight: 600;
    font-size: 14px;
    background-color: #ffffff;
  }

  &__add {
    padding: 40px;
    background-color: #ffffff;
    cursor: pointer;

    > div {
      padding: 20px;
      border: 2px solid #cccccc;
      border-radius: 5px;
      text-align: center;
      color: green;

      .icon-plus {
        font-size: 3em;
        font-weight: 300;
      }
    }
  }

  &__buttons {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 30px;

    a {
      display: flex;
      align-items: center;
      border-radius: 5px;
      padding: 10px 15px;

      &:first-child {
        background-color: #ffffff;
        color: green;
      }

      &:last-child {
        background-color: green;
        color: #ffffff;

        svg {
          width: 1em;
          height: 1em;
          margin-left: 5px;
          fill: #ffffff;
        }
      }
    }
  }
}
</style>
