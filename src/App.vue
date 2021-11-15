<template>
  <TheNavigation />
  <router-view />
</template>

<script>
  import TheNavigation from '@/components/TheNavigation.vue'

  export default {
    components: {
      TheNavigation
    },
  }
</script>

<style>
  #app{
    height: 100vh
  }
  @import url('https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css');
</style>