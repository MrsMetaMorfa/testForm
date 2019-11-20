<template>
  <aside class="container_column-small">
    <div class="p_logo"></div>
    <nav class="p_nav">
      <ul class="p_nav-list">
        <li class="p_nav-list__item">
          <nuxt-link to="/">
            <img src="" alt="" class="img" width="40px" height="40px">
            <span>Опросы</span>
          </nuxt-link>
        </li>
        <li class="p_nav-list__item current">
          <nuxt-link to="/">
            <img src="" alt="" class="img" width="40px" height="40px">
            <span>Пользователи</span>
          </nuxt-link>
        </li>
        <li class="p_nav-list__item">
          <nuxt-link to="/">
            <img src="" alt="" class="img" width="40px" height="40px">
            <span>Чёрные списки</span>
          </nuxt-link>
        </li>
        <li class="p_nav-list__item">
          <nuxt-link to="/">
            <img src="" alt="" class="img" width="40px" height="40px">
            <span>Колл-центр</span>
          </nuxt-link>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script>
  export default {
      name: 'AsideMenu'
  }
</script>

<style lang="sass">
  .container_column-small
    position: fixed
    top: 0
    left: 0
    bottom: 0
    width: 180px
    border-right: 1px solid darkgray
    padding: 10px

  .p_logo
    display: block
    width: 40px
    height: 40px
    border-radius: 50%
    background: red
    margin: 0 auto 40px

  .p_nav-list
    list-style-type: none
    padding: 0 10px
    margin: 0
    &__item
      width: 100%
      margin-bottom: 15px
      a
        display: block
        border: 3px solid transparent
        border-radius: 8px
        padding: 10px
        text-align: center
        color: black
        font-size: 16px
        text-decoration: none
        .img
          margin: 0 auto 10px
        &:hover, &:focus
          background-color: lightgrey
          border-color: lightgrey
          font-weight: 700
      &.current a
        color: gold
        border-color: gold
        &:hover, &:focus
          background: transparent

</style>

