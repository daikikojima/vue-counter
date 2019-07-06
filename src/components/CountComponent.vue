<template>
  <div class="hello">
    <h1 class="number">{{ count }}</h1>
    <el-row>
      <el-col :span="12">
        <el-button class="match-button" type="primary" @click="onClickMinus"
          >-</el-button
        >
      </el-col>
      <el-col :span="12">
        <el-button class="match-button" type="danger" @click="onClickAdd"
          >+</el-button
        >
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <el-button class="match-button" type="success" @click="onClear"
          >clear</el-button
        >
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "CountComponent",
  props: ["count", "update"],
  methods: {
    onClickMinus() {
      this.update("DECREMENT");
    },
    onClickAdd() {
      this.update("INCREMENT");
    },
    onClear() {
      this.update("CLEAR");
    }
  }
};
</script>

<style scoped>
h1.number {
  font-size: 8em;
}
.match-button {
  width: 100%;
  height: 100px;
  font-size: 5em;
}
</style>
