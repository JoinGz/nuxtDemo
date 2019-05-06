<template>
  <div>
    <navbar :activeIndex2="'2-2'" />
    <nuxt />
  </div>
</template>
<script>
import navbar from '~/components/nav.vue'
export default {
  components: {
    navbar
  },
  methods:{
  }
}
</script>

<style>
</style>
