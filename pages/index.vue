<template>
  <section class="container">
    <AsideMenu />
    <main class="container_column-huge">
      <Header />
      <Breadcrumbs />
      <Tabs />
    </main>
  </section>
</template>

<script>
import AsideMenu from '~/components/AsideMenu.vue'
import Header from '~/components/Header.vue'
import Breadcrumbs from "../components/Breadcrumbs";
import Tabs from "../components/Tabs";

export default {
    components: {
        Tabs,
        Breadcrumbs,
        AsideMenu,
        Header
    },
    data: function () {
        return {
            'name': 'Title',
            'description': 'Description'
        }
    }
}

</script>

<style lang="sass">
.container
  min-height: 100vh
  position: relative
  &--flex
    display: flex

.img
  display: block
  max-width: 100%
  max-height: 100%
  background-color: gray
  background-image: linear-gradient(to bottom left, transparent 0, transparent 49%, darkslategray 49%, darkslategray 51%, transparent 51%, transparent 0), linear-gradient(to bottom right, transparent 0, transparent 49%, darkslategray 49%, darkslategray 51%, transparent 51%, transparent 0)
  background-repeat: no-repeat
  background-position: center


.container_column-huge
  margin-left: 180px
  padding: 15px

.hidden-label
    font-size: 0
    line-height: 0
    width: 0
    height: 0
    visibility: hidden
    opacity: 0
    position: absolute


</style>

