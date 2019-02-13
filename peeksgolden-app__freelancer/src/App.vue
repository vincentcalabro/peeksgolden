<style lang="scss">
  @import 'src/assets/css/base.scss';
</style>

<template>
  <v-app>
    <core-toolbar />

    <core-view />

    <core-footer />
  </v-app>
</template>

<script>
export default {
  components: {
    CoreFooter: () => import('@/components/core/Footer'),
    CoreToolbar: () => import('@/components/core/Toolbar'),
    CoreView: () => import('@/components/core/View')
  }
}
</script>
