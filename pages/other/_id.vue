<template>
  <div>
    当前的router参数是：{{id}}
    <p>{{num}}</p>
  </div>
</template>
<script>
export default {
  name: 'other',
  asyncData ({ params }) {
    //  返回的对象会覆盖data里面定义了值的对象
    return params
  },
  data () {
    return {
      id: 6,
      num: 99
    }
  }
}
</script>
<style lang="less" scoped>

</style>

