<template>
  <component
    :is="tag"
    class="headline v-heading mb-2 font-weight-black"
  >
    <slot />
  </component>
</template>

<script>
export default {
  props: {
    tag: {
      type: String,
      default: 'h1'
    }
  }
}
</script>

<style lang="sass">
  .v-heading
    letter-spacing: 2px !important
</style>
