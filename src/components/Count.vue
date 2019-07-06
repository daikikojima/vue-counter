<template>
  <div class="hello">
    <h1 class="number">{{ count }}</h1>
    <el-row>
      <el-col :span="12">
        <el-button class="match-button" type="primary" @click="minus"
          >-</el-button
        >
      </el-col>
      <el-col :span="12">
        <el-button class="match-button" type="danger" @click="plus"
          >+</el-button
        >
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <el-button
          class="match-button"
          type="success"
          size="medium"
          @click="clear"
          >clear</el-button
        >
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "Count",
  data() {
    return {
      count: 0
    };
  },
  methods: {
    plus() {
      this.count++;
    },
    minus() {
      this.count--;
    },
    clear() {
      this.count = 0;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h1.number {
  font-size: 8em;
}
.match-button {
  width: 100%;
  height: 100px;
  font-size: 5em;
}
</style>
