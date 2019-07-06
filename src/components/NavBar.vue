<template>
  <el-menu
    :default-active="$route.path"
    class="el-menu-demo"
    mode="horizontal"
    background-color="#545c64"
    text-color="#fff"
    active-text-color="#ffd04b"
  >
    <el-menu-item class="tab" index="/">
      <router-link to="/">Count App (with data)</router-link>
    </el-menu-item>
    <el-menu-item class="tab" index="/container">
      <router-link to="/container">Count App (with props)</router-link>
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
