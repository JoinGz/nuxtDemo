<template>
  <el-menu :default-active="activeIndex2" class="el-menu-demo" @select="handleSelect" mode="horizontal" background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
    <el-menu-item index="1">
      <nuxt-link to="/about">关于</nuxt-link>
    </el-menu-item>
    <el-submenu index="2">
      <template slot="title">我的工作台</template>
      <el-menu-item index="2-1">选项1</el-menu-item>
      <el-menu-item index="2-2">选项2</el-menu-item>
      <el-menu-item index="2-3">选项3</el-menu-item>
      <el-submenu index="2-4">
        <template slot="title">选项4</template>
        <el-menu-item index="2-4-1">选项1</el-menu-item>
        <el-menu-item index="2-4-2">选项2</el-menu-item>
        <el-menu-item index="2-4-3">选项3</el-menu-item>
      </el-submenu>
    </el-submenu>
    <el-menu-item index="3" >消息中心</el-menu-item>
    <el-menu-item index="4">
      <a>订单管理</a>
    </el-menu-item>
  </el-menu>
</template>
<script>
export default {
  name: 'navBar',
  props: ['activeIndex2'],
  methods: {
    handleSelect (data) {
      if (data.indexOf('2') >= 0) {
        this.$router.push('/')
      } else if (data.indexOf('3') >= 0) {
        this.$router.push('/other/3')
      } else if (data.indexOf('4') >= 0) {
        this.$router.push('/threeRouter')
      }
    }
  }
}
</script>

<style>
</style>
