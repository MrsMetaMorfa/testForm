<template>
  <div class="p_tabs">
    <ul class="p_tabs-list container--flex">
      <li class="p_tabs-list__item" :class='{active: buttonParamsActive}'>
        <button class="btn-tab" type="button" @click="setParamsActive">Параметры</button>
      </li>
      <li class="p_tabs-list__item" :class='{active: buttonQuestionActive}'>
        <button class="btn-tab" type="button" @click="setQuestionActive">Вопросы</button>
      </li>
      <li class="p_tabs-list__item" :class='{active: buttonLogicActive}'>
        <button class="btn-tab" type="button" @click="setLogicActive">Логика</button>
      </li>
      <li class="p_tabs-list__item" :class='{active: buttonConditionActive}'>
        <button class="btn-tab" type="button" @click="setConditionActive">Условия</button>
      </li>
      <li class="p_tabs-list__item" :class='{active: buttonRespondentsActive}'>
        <button class="btn-tab" type="button" @click="setRespondentsActive">Респонденты</button>
      </li>
    </ul>
    <div class="p_tabs__content">
      <div class="tab-content" v-if="tabParamsActive">
        Params content coming soon
      </div>
      <div class="tab-content" v-if="tabQuestionActive">
        Question content coming soon
      </div>
      <div class="tab-content" v-if="tabLogicActive">
        Logic content coming soon
      </div>
      <div class="tab-content" v-if="tabConditionActive">
        Conditions content coming soon
      </div>
      <Respondents v-if="tabRespondentsActive" />
    </div>
  </div>
</template>

<script>
  import Respondents from "./Respondents";
  export default {
      name: 'Tabs',
      components: {Respondents},
      data: function () {
          return {
              buttonParamsActive: false,
              buttonQuestionActive: false,
              buttonLogicActive: false,
              buttonConditionActive: false,
              buttonRespondentsActive: true,
              //
              tabParamsActive: false,
              tabQuestionActive: false,
              tabLogicActive: false,
              tabConditionActive: false,
              tabRespondentsActive: true,
          }
      },
      methods: {
          setParamsActive: function ($event) {
              if (!$event || !$event.target.classList.contains('active')) {
                  this.buttonParamsActive = true;
                  this.buttonQuestionActive = false;
                  this.buttonLogicActive = false;
                  this.buttonConditionActive = false;
                  this.buttonRespondentsActive = false;

                  this.tabParamsActive = true;
                  this.tabQuestionActive = false;
                  this.tabLogicActive = false;
                  this.tabConditionActive = false;
                  this.tabRespondentsActive = false;
              }
          },
          setQuestionActive: function ($event) {
              if (!$event || !$event.target.classList.contains('active')) {
                  this.buttonParamsActive = false;
                  this.buttonQuestionActive = true;
                  this.buttonLogicActive = false;
                  this.buttonConditionActive = false;
                  this.buttonRespondentsActive = false;

                  this.tabParamsActive = false;
                  this.tabQuestionActive = true;
                  this.tabLogicActive = false;
                  this.tabConditionActive = false;
                  this.tabRespondentsActive = false;
              }
          },
          setLogicActive: function ($event) {
              if (!$event || !$event.target.classList.contains('active')) {
                  this.buttonParamsActive = false;
                  this.buttonQuestionActive = false;
                  this.buttonLogicActive = true;
                  this.buttonConditionActive = false;
                  this.buttonRespondentsActive = false;

                  this.tabParamsActive = false;
                  this.tabQuestionActive = false;
                  this.tabLogicActive = true;
                  this.tabConditionActive = false;
                  this.tabRespondentsActive = false;
              }
          },
          setConditionActive: function ($event) {
              if (!$event || !$event.target.classList.contains('active')) {
                  this.buttonParamsActive = false;
                  this.buttonQuestionActive = false;
                  this.buttonLogicActive = false;
                  this.buttonConditionActive = true;
                  this.buttonRespondentsActive = false;

                  this.tabParamsActive = false;
                  this.tabQuestionActive = false;
                  this.tabLogicActive = false;
                  this.tabConditionActive = true;
                  this.tabRespondentsActive = false;
              }
          },
          setRespondentsActive: function ($event) {
              if (!$event || !$event.target.classList.contains('active')) {
                  this.buttonParamsActive = false;
                  this.buttonQuestionActive = false;
                  this.buttonLogicActive = false;
                  this.buttonConditionActive = false;
                  this.buttonRespondentsActive = true;

                  this.tabParamsActive = false;
                  this.tabQuestionActive = false;
                  this.tabLogicActive = false;
                  this.tabConditionActive = false;
                  this.tabRespondentsActive = true;
              }
          },

      }
  }
</script>

<style lang="sass">
  .p_tabs
    &-list
      list-style-type: none
      margin: 0
      padding: 0
      border-bottom: 1px solid gold
      justify-content: space-around
      &__item
        margin: 0 10px
        .btn-tab
          display: block
          border-radius: 0
          border: solid transparent
          border-width: 0 0 3px 0
          line-height: 30px
          padding: 0 10px
          background: transparent
          color: olivedrab
          outline: none
          &:hover, &:focus
            font-weight: 700
        &.active .btn-tab
          font-weight: 700
          border-bottom-color: gold
          color: black

</style>

