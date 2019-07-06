<template>
  <el-menu
    :default-active="$route.path"
    :router="true"
    class="el-menu-demo"
    mode="horizontal"
    background-color="#545c64"
    text-color="#fff"
    active-text-color="#ffd04b"
  >
    <el-menu-item class="tab" index="/">
      Count App (with data)
    </el-menu-item>
    <el-menu-item class="tab" index="/container">
      Count App (with props)
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style lang="scss" scoped>
.el-menu-demo {
  display: flex;
  justify-content: space-around;
  .tab {
    width: 100%;
  }
}
</style>
