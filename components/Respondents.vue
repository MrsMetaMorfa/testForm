<template>
  <div class="tab-content">
    <h2 class="tab-content_title">Добавить условие</h2>
    <div class="tab-content_conditions">
      <RespondentsCondition />
    </div>
    <button class="btn-add" type="button" @click="addNewCondition">
      <span class="btn-add__icon">+</span>
      <span>Нажмите, чтобы добавить условие выборки.</span>
      <span>Все условия связываются с собой логическими "И"</span>
    </button>
  </div>
</template>

<script>
  import RespondentsCondition from "./RespondentsCondition";
  export default {
      name: 'Respondents',
      components: {RespondentsCondition},
      methods: {
          addNewCondition: function ($event) {
              $event.previousSibling.append(RespondentsCondition);
          }
      }
  }
</script>

<style lang="sass">
  .tab-content
    border-radius: 0 6px 6px 0
    box-shadow: 0 5px 5px 0 darkgray
    padding-bottom: 10px
    &_title
      padding: 10px
      color: gray
      font-weight: 700
      font-size: 1em
    .btn-add
      display: block
      padding: 15px
      background: transparent
      color: green
      cursor: pointer
      border: 1px solid darkgray
      margin: 15px 15px 0
      width: calc(100% - 30px)
      span
        display: block
        text-align: center
        width: 100%
        &.btn-add__icon
          font-size: 30px
          line-height: 1

</style>

