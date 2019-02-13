<template>
  <div>
    <welcome />
    <ingredients />
    <about-me />
    <get-in-touch />
  </div>
</template>

<script>
export default {
  components: {
    AboutMe: () => import('@/components/AboutMe'),
    GetInTouch: () => import('@/components/GetInTouch'),
    Ingredients: () => import('@/components/Ingredients'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
