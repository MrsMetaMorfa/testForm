<template>
  <header class="container--flex p_header">
    <form class="p_header__search container--flex">
      <label for="pageSearch" class="hidden-label">Поиск по системе</label>
      <input type="search" name="search" id="pageSearch" placeholder="Поиск по системе">
      <button class="btn-search" type="submit" aria-label="Найти">
        <img src="" alt="" class="img" width="30px" height="30px">
      </button>
    </form>
    <div class="p_header__user container--flex">
      <div class="user_avatar">
        <img src="" alt="" class="img" width="40px" height="40px">
      </div>
      <div class="user_info">
        <p class="user_name">Alexander S.</p>
        <p class="user_status">Administrator</p>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
      name: 'Header'
  }
</script>

<style lang="sass">
  .p_header
    justify-content: space-between
    align-content: center
    margin-bottom: 20px
    &__search
      width: 60%
      min-width: 400px
      background: white
      border: 1px solid lightgrey
      border-radius: 6px
      overflow: hidden
      input
        width: calc(100% - 50px)
        border: none
        line-height: 20px
        padding: 10px
        display: block
      .btn-search
        display: block
        padding: 10px
        border: none
        border-radius: 0
        background: transparent
        cursor: pointer
    &__user
      margin-left: 15px
      align-items: center
      .user_avatar
        border-radius: 50%
        margin: 0 10px 0 0
        overflow: hidden
      .user_info
        .user_name
          font-weight: 700
        .user_status
          font-size: 0.8em

</style>

