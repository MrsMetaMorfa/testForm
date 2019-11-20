<template>
  <ul class="p_breadcrumbs container--flex">
    <li class="p_breadcrumbs__item">
      <nuxt-link to="/" aria-label="Home">
        <img src="" alt="" class="img" width="20px" height="20px">
      </nuxt-link>
    </li>
    <li class="p_breadcrumbs__item divider">&rarr;</li>
    <li class="p_breadcrumbs__item">
      <nuxt-link to="/">Опросы</nuxt-link>
    </li>
    <li class="p_breadcrumbs__item divider">&rarr;</li>
    <li class="p_breadcrumbs__item current">Add new</li>
  </ul>
</template>

<script>
  export default {
      name: 'Breadcrumbs'
  }
</script>

<style lang="sass">
  .p_breadcrumbs
    align-items: center
    list-style-type: none
    padding: 0
    margin: 0 auto 20px 0
    line-height: 1
    font-size: 0.75em
    &__item
      margin-right: 6px
      .nuxt-link-active
        color: black
        text-decoration: none
        &:hover, &:focus
          text-decoration: underline
      &.divider
        font-weight: 700
      &.current
        opacity: 0.5
</style>

